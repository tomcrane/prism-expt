# Test

This is a code block with line numbers
https://prismjs.com/plugins/line-numbers/

{: .line-numbers }
```javascript

var x = 10;
alert(x);

```

How do we include a file for highlighting? This is done client side:
https://prismjs.com/plugins/file-highlight/

{: .line-numbers data-src="manifest.json" }
```json
```

And now a block with some highlights. 
https://prismjs.com/plugins/line-highlight/

{: .line-numbers data-src="manifest.json" data-line="169-182" }
```json
```

Can we restrict the code snippet to just a part of the source file?
(We may need to write a prism plugin for some of these variations)
I just made up `data-scroll-to-line`- it would need to identify the line referenced, then scroll it into view in the div with max-height.

{: .line-numbers data-src="manifest.json" data-line="82,90" style="max-height:350px" data-scroll-to-line="81" }
```json
```
