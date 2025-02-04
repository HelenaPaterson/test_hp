# Glossary

You can use the `glossary()` function to automatically link to a term in the [psyTeachR glossary](https://psyteachr.github.io/glossary/) or make your own project-specific glossary.

This will create a link to the glossary and include a tooltip with a short definition when you hover over the term. Use the following syntax in inline r: `glossary("word")`. For example, common <a href='https://psyteachr.github.io/glossary/d#data-type' target='_blank' class='glossary' title='The kind of data represented by an object.'>data types</a> are <a href='https://psyteachr.github.io/glossary/i#integer' target='_blank' class='glossary' title='A data type representing whole numbers.'>integer</a>, <a href='https://psyteachr.github.io/glossary/d#double' target='_blank' class='glossary' title='A data type representing a real decimal number'>double</a>, and <a href='https://psyteachr.github.io/glossary/c#character' target='_blank' class='glossary' title='A data type representing strings of text.'>character</a>.

If you need to link to a definition, but are using a different form of the word, add the display version as the second argument (`display`). You can also override the automatic short definition by providing your own in the third argument (`def`). Add the argument `link = FALSE` if you just want the hover definition and not a link to the psyTeachR glossary.


```r
glossary("data type", 
         def = "My custom definition of data types")
```

[1] "<a class='glossary' title='My custom definition of data types'>data type</a>"

You can add a glossary table to the end of a chapter with the following code. It creates a table of all terms used in that chapter previous to the `glossary_table()` function. It uses `kableExtra()`, so if you use it in a code chunk, set `results='asis'`.

<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r, echo=FALSE, results='asis'}</code></pre>

```r
glossary_table()
```

<pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>

<table class="table" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> term </th>
   <th style="text-align:left;"> definition </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> <a href="https://psyteachr.github.io/glossary/c#character" target="_blank">character</a> </td>
   <td style="text-align:left;"> A data type representing strings of text. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> <a href="https://psyteachr.github.io/glossary/d#data-type" target="_blank">data-type</a> </td>
   <td style="text-align:left;"> My custom definition of data types </td>
  </tr>
  <tr>
   <td style="text-align:left;"> <a href="https://psyteachr.github.io/glossary/d#double" target="_blank">double</a> </td>
   <td style="text-align:left;"> A data type representing a real decimal number </td>
  </tr>
  <tr>
   <td style="text-align:left;"> <a href="https://psyteachr.github.io/glossary/i#integer" target="_blank">integer</a> </td>
   <td style="text-align:left;"> A data type representing whole numbers. </td>
  </tr>
</tbody>
</table>



If you want to contribute to the glossary, fork the [github project](https://github.com/PsyTeachR/glossary), add your terms and submit a pull request, or suggest a new term at the [issues page](https://github.com/PsyTeachR/glossary/issues).
