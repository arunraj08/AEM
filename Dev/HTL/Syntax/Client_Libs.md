Client Library
-----------------

Invoke Client Library

1) JS

```html  
  <sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html" 
       data-sly-call="${clientLib.js @categories='we.train.all'}">
  </sly>
```

2) CSS

```html  
  <sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html" 
       data-sly-call="${clientLib.css @categories='we.train.all'}">
  </sly>
```

3) ALL

```html  
  <sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html" 
       data-sly-call="${clientLib.all @categories='we.train.all'}">
  </sly>
```


Attributes
------------
1) categories : To identify respective client library

2) Dependency : This is list of other client library categories on which this library depends on.
   Ex: Scripts depends on jquery

3) Embed : Used to embed code form other libraries
    Ex: cl1 embeds cl2 = cl1 + cl2
