# Jekyll Boom! Starter Theme V2

A more "advanced" starter theme for books, see the 
[Jekyll Boom! Starter Theme V1](https://github.com/henrythemes/jekyll-boom-theme) for
a more "basic" HTML-only version.
The V2 includes:

1) Uses plain text in Markdown for all chapters, preface, table of contents, index, etc.

For example the preface in the "basic" HTML version:

```html
<p>This is a sample document whose purpose is to show how CSS can be
used to print a book. To make the document more lively, excerpts from
the third edition of &ldquo;Cascading Style Sheets &mdash; designing
for tbe Web&rdquo; have been included.<span class="footnote"> That
book <em>was</em> produced using the methods described in the
document, and it was published by Addison-Wesley in 2005.</span> The
excerpts have been selected for their example values and they appear,
in this document, out of order.</p>

<p>The PDF version of this document is produced directly from the HTML
and CSS sources by the Prince formatter.</p>
```

becomes in Markdown:

```markdown
This is a sample document whose purpose is to show how CSS can be
used to print a book. To make the document more lively, excerpts from
the third edition of "Cascading Style Sheets - designing
for the Web" have been included.[^1] The
excerpts have been selected for their example values and they appear,
in this document, out of order.

The PDF version of this document is produced directly from the HTML
and CSS sources by the Prince formatter.

[^1]: That book _was_ produced using the methods described in the
document, and it was published by Addison-Wesley in 2005.
```


2) "Simplified" and "cleaned up" styles and markup to work along with the Markdown conventions and best practices 




## Live Demo

See a live demo @ [`henrythemes.github.io/jekyll-boom-theme-v2` »](http://henrythemes.github.io/jekyll-boom-theme-v2)




## Markdown Notes

**Footnotes**

```html
<span class="footnote"> That
book <em>was</em> produced using the methods described in the
document, and it was published by Addison-Wesley in 2005.</span>
```

becomes

```
[^1]

...

[^1]: That book _was_ produced using the methods described in the
document, and it was published by Addison-Wesley in 2005.
```

**Inline (Code) Spans**

``` html
<span class="element">img</span>
```

becomes

```
`img`{:.element}
```


## "Custom" Markdown Macros / Helpers

```
`img`{:.element}
`font-size`{:.property}
`font-family: monospace`{:.css}
```

becomes

```
{{ element img }}         =>  <span class="element">img</span>
{{ property font-size }}  =>  <span class="property">font-size</span>
{%css%} font-family: monospace {%endcss%}  =>  <span class="css">font-family: monospace</span>
```


### References

```
["CSS Specifications"](#specs){:.pageref}
```

becomes

```
{{ pageref "CSS Specifications", specs }}   or
@pageref("CSS Specifications", specs)      ???  -- see pandoc ref style??
```




## Boom! Build & Update Notes

to be done



### More Themes

See the [Dr. Jekyll's Themes](https://drjekyllthemes.github.io) directory.

### More Quick Starter Wizard Scripts

See the [Mr. Hyde's Scripts](https://github.com/mrhydescripts/scripts) library.


## Meta

**Questions? Comments?**

Post them to the [wwwmake forum](http://groups.google.com/group/wwwmake). Thanks!
