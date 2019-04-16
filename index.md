# Test

This is a code block with line numbers
<https://prismjs.com/plugins/line-numbers/>

{: .line-numbers }
```javascript

var x = 10;
alert(x);

```

How do we include a file for highlighting? This is done client side:
<https://prismjs.com/plugins/file-highlight/>
This allows us to include full working dereferenceable code samples, and use them in the narrative without duplication.
[download this manifest](manifest.json) 

{: .line-numbers data-src="manifest.json" }
```json
```

And now a block with some highlights - combining two plugins for prism.js.
<https://prismjs.com/plugins/line-highlight/>

{: .line-numbers data-src="manifest.json" data-line="169-182" }
```json
```

Can we restrict the code snippet to just a part of the source file?

(We may need to write a prism plugin for some of these variations)

I just made up `data-scroll-to-line`- it would need to identify the line referenced, then scroll it into view in the div with max-height. You'll have to manually scroll to line 81 for now.
This mechanism allows the narrative to focus on the significant part of the code sample; we need a window on the code.

{: .line-numbers data-src="manifest.json" data-line="82,90" style="max-height:350px" data-scroll-to-line="81" }
```json
```

We could also customise the file-highlight plugin to load the source and trim it, rather than a viewport on it (i.e., no scrollbars). Probably need both mechanisms.
