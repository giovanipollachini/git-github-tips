Link to tutorial:
https://guides.github.com/features/mastering-markdown/


It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to Google!](http://google.com)



# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag



*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_



* Item 1
* Item 2
  * Item 2a
  * Item 2b
  
  
  
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
   
   
   
![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)



http://github.com - automatic!
[GitHub](http://github.com)



As Kanye West said:

> We're living the future so
> the present is our past.



I think you should use an
`<addr>` element here instead.



```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```



    function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
    
    
    


- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item



First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column



~~this~~

## Collapsible sections:

Reference: https://gist.github.com/pierrejoubert73/902cc94d79424356a8d20be2b382e1ab

### A collapsible section containing markdown
<details>
  <summary>Click to expand!</summary>
  
  #### Heading
  1. A numbered
  2. list
     * With some
     * Sub bullets
</details>

**NB:** Make sure you have an **empty line** after the closing `</summary>` tag, otherwise the markdown/code blocks won't show correctly.

**NB**: Make sure you have an **empty line** after the closing `</details>` tag if you have multiple collapsible sections.

   
   
