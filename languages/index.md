# Language comparision 


## Data structures and types 

### Arrays

<table>
  <thead>
  <tr style="height:20px;">
    <td class="s0" dir="ltr">Language</td>
    <td align="center" colspan="3">Array</td>
  </tr>
  </thead>
  <tbody>
  <tr style="height:20px;">
    <td class="s0" dir="ltr">Java 9</td>
    <td class="s2" dir="ltr">  
       <pre lang="java">Type[] arr; Type arr[];</pre>
    </td>
    <td class="s2" align="center" dir="ltr">
      <pre lang="java">{a, b, c}</pre>
    </td>
    <td class="s2" dir="ltr">
      <pre lang="java">new Type[] {a, b, c}</pre>
    </td>
  </tr>
  <tr style="height:20px;" style="background-color:#FFF">
    <td class="s3" dir="ltr">Kotlin</td>
    <td class="s2" dir="ltr">
      <pre lang="Kotlin"> var arr: Array&lt;T&gt; </pre>
    </td>
    <td class="s2" align="center" dir="ltr">
      <pre lang="Kotlin"> arrayOf(a, b, c); </pre>
    </td> 
    <td class="s2" dir="ltr"></td>
  </tr>
  <tr style="height:20px;">
    <td class="s0" dir="ltr">JS</td>
    <td class="s4" dir="ltr"></td>
    <td class="s2" align="center" dir="ltr"> 
       <pre lang="javascript"> [a, b, c] </pre>
    </td>
    <td class="s2" dir="ltr">
      <pre lang="javascript"> Array(a, b, c) </pre>
    </td>
  </tr>
  <tr style="height:20px;">
    <td class="s0" dir="ltr">Python 3.8</td>
    <td class="s4" dir="ltr"></td>
    <td class="s2" align="center" dir="ltr">
      <pre lang="python"> array([a, b, c]) </pre>
    </td>
    <td class="s2" dir="ltr"></td>
  </tr>
  <tr style="height:20px;">
    <td class="s3" dir="ltr">C/C++ 11</td>
    <td class="s2" dir="ltr">
       <pre lang="c++"> Type arr[]; </pre>
    </td>
    <td class="s2" align="center" dir="ltr">
       <pre lang="c++"> {a, b, c} </pre>
    </td>
    <td class="s2" dir="ltr">
       <pre lang="c++"> (Type[]) { a, b, c } </pre>
    </td>
  </tr>
  <tr style="height:20px;">
    <td class="s3" dir="ltr">Bash</td>
    <td class="s5" dir="ltr"></td>
    <td class="s6" align="center" dir="ltr">
      <pre lang="bash"> (a, b, c) </pre>
    </td>
    <td class="s6" dir="ltr"></td>
  </tr>
  </tbody>
</table>

### Dictionaries

<table>
  <thead>
  <tr style="height:20px;">
    <td class="s0" dir="ltr">Language</td>
    <td align="center" colspan="3">Map/Dictionary</td>
  </tr>
  </thead>
  <tbody>
  <tr style="height:20px;">
    <td class="s0" dir="ltr">Java 9</td>
    <td class="s2" dir="ltr">
       <pre lang="java">  Map&lt;K, V&gt; map; </pre>
    </td>
    <td class="s2" dir="ltr">
       <pre lang="java">  Map.of(key, value, key2, value2) </pre>
    </td>
    <td class="s2" dir="ltr">
       <pre lang="java">  new HashMap&lt;K, V&gt;() </pre>
    </td>
  </tr>
  <tr style="height:20px;" style="background-color:#FFF">
    <td class="s3" dir="ltr">Kotlin</td>
    <td class="s2" dir="ltr">
      <pre lang="Kotlin"> val map: Map&lt;K, V&gt; </pre>
    </td>
    <td class="s2" dir="ltr">
      <pre lang="Kotlin"> mapOf(key to value, key1 to value2) </pre>
    </td>
    <td class="s2" dir="ltr">
       <pre lang="Kotlin">  HashMap&lt;K, V&gt;() </pre>
    </td>
  </tr>
  <tr style="height:20px;">
    <td class="s0" dir="ltr">JS</td>
    <td class="s4" dir="ltr"></td>
    <td class="s2" dir="ltr">
       <pre lang="javascript">  { "k" : v, "k1" : v }  </pre> 
    </td>
    <td class="s2" dir="ltr"></td>
  </tr>
  <tr style="height:20px;">
    <td class="s0" dir="ltr">Python 3.8</td>
    <td class="s2" dir="ltr"></td>
    <td class="s2" dir="ltr">
      <pre lang="python"> { k : v, k1 : v }  </pre> 
    </td>
    <td class="s2" dir="ltr"></td>
  </tr>
  <tr style="height:20px;">
    <td class="s3" dir="ltr">C/C++ 11</td>
    <td class="s2" dir="ltr">
      <pre lang="c++"> std::map&lt;k, v&gt; map </pre> 
    </td>
    <td class="s2" dir="ltr"> 
      <pre lang="c++">  { {k, v}, {k, v} } </pre> 
    </td>
    <td class="s2" dir="ltr"></td>
  </tr>
  <tr style="height:20px;">
    <td class="s3" dir="ltr">Bash</td>
    <td class="s7" align="center" colspan="3">N/A</td>
  </tr>
  </tbody>
</table>

