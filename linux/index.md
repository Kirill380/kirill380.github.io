## Usefull bash comands

1. Show disk usage and available space on Linux file system  <br>
```bash
df -f
```

2. Summarized space usage in current directory <br>
```bash
du -sh
```

3. Show disk usage of folders in current directory  <br>
```bash
du -h --max-depth=1 | sort -hr
```

## Usefull links
1. [Linux shell scripting](https://www.linkedin.com/learning/learning-linux-shell-scripting-2)

## Bash pazzlers

1. Set image tags based on feature branch 
```bash
function process_dependent_tags () {
    TRG_BRANCH=$1
    TRG_DREG_USER=$2
    TRG_DREG_PASSWORD=$3
    TRG_DREG_URL=$4

    TRG_OIFS="$IFS"
    IFS=$'\n'

    for trg_str in $(grep -E "\s*image:" ${@:5}); do
      TRG_IMG_DEF=$(echo $trg_str | sed -E "s/^(.*:).*image:\s*(.*)\s*.*$/\1\2/" | sed "s%dregistry.com/%%")
      TRG_FULL_STR=$(echo $trg_str | sed -E "s/.*?\.yml:(.{1,})/\1/")
      TRG_FILE=$(echo $trg_str | awk -F ":" '{ print $1 }')
      TRG_IMG=$(echo $TRG_IMG_DEF | awk -F ":" '{ print $2 }' )
      TRG_IMG_TAG=$(echo $TRG_IMG_DEF | awk -F ":" '{ print $3 }')
      TRG_IMG_TAG="${TRG_IMG_TAG%%*( )}"

      if [ "x$TRG_IMG_TAG" == "x" ]; then
        TRG_DREG_TAG=$(curl -X GET --insecure --user $TRG_DREG_USER:$TRG_DREG_PASSWORD ${TRG_DREG_URL}/${TRG_IMG}/tags/list 2>/dev/null | jq ".tags[]" 2>/dev/null | sed 's/"//g' | grep -E "^$TRG_BRANCH-[0-9]{1,}" | sort --reverse | head -n 1)
        TRG_FINAL_TAG=${TRG_IMG_TAG:-${TRG_DREG_TAG:-latest}}
        if [[ "x$TRG_FINAL_TAG" != "x$TRG_IMG_TAG" ]]; then
          if [[ "x$TRG_FINAL_TAG" != "xlatest" ]]; then
            echo "Using $TRG_FINAL_TAG for $TRG_IMG"
            NEW_STR=$(echo $(echo $TRG_FULL_STR | sed -E "s%^(\s*image:\s{1,}$TRG_IMG)%\1%"):$TRG_FINAL_TAG)
            sed -i "s%$TRG_FULL_STR%$NEW_STR%" $TRG_FILE
          fi
        fi
      fi
    done

    IFS="$TRG_OIFS"
}
```

