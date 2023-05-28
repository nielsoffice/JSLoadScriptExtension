# JSLoadScriptExtension
JavaScript jQuery load or import or get extension JavaScript file within the folder or CDN

``` This only work in server running ```

```PHP
 // Data or file structure 
 -- Main 
    -- JS
       -- script1.js
       -- script2.js
    -- IMG
    -- CSS
  - index.html
  - about.html
```

```JS
// script1.js File
 const deep = function( data ) {
 
   this.data = data;
	
 }

 deep.prototype.init = function() {
  
   let extention = this.data;
   console.log(extention);
   
 }	
 
const deeply = function( d )  {
  
  const withDeep = new deep( d );
        withDeep.init();

} 
```

```HTML
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.4/jquery.min.js"></script>
<script>
 jQuery(document).ready(function(){
   
  $.getScript('script1.js', function() { 
    jQuery('#event').bind('click', function() {
        
       deeply('This is js-extension 2');
  
    });  
  });

 });
</script> 
</head>
<body>

 <button id="event">Implement</button>
  
</body>
</html>
```
