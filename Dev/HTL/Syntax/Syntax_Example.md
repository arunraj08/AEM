AEM Slightly
-------------
1. Sightly comment.
2. Sightly expression
3. Sightly attributes
4. Sly element

Sightly comment : 
-----------------
	Recommended over html comments.
	<!--/* An HTL Comment */-->
	<!-- An HTML Comment -->

Sightly expression: ${}
-------------------
  Ex : 
  ${properties.jcr:title}
  ${!currentPage.hasChild}
  ${varOne || varTwo}
  ${varOne == varTwo}

Sly element:
-------------- 
 1) It removes from the output
 2) Use it for all elements that are not part of markup.


Sightly attributes: 
--------------------
 1) data-sly-use/call/repeat/text/list/test/include/resource.

 2) data-sly-text : Replaces the content of HTML elements with the specified text.

    Eg : 
  ```html
   <div data-sly-text= "${currentPage.title}">Title Page </div>
  ```

 3) data-sly-list : Repeats the child elements.

    Eg: 
 {::nomarkdown}
   <ul data-sly-list="${[1,2,3,4]}">
		  <li>${item}</li>
		</ul>
{:/}

 4) data-sly-repeat : Repeats the same element

 	Eg: 
 {::nomarkdown}
   <ul>
 		 <li data-sly-repeat.child="currentPage.listChildren">${child.title}</li>
  </ul>
 {:/}
 
 5) data-sly-test : To hide or show HTML element

 	Eg :
{::nomarkdown} 	 
   <div data-sly-test="${wcmmode.edit}"> This is edit mode </div>
 {:/}

 6) data-sly-include : To include other file (jsp/html)

    Eg: 
{::nomarkdown}
    <sly data-sly-include="test.html"></sly>
{:/}

 7) data-sly-resource : To include AEM components

 	Eg: 
{::nomarkdown}
 	<sly data-sly-resource=${'par' @ resourceType = 'foundation/components/parsys' }>
 	    </sly>
{:/}

 8) data-sly-use : To invoke helper file.

 	Eg: 
{::nomarkdown}
 <div data-sly-use.comp = "logic.js">
 		  ${comp.myTitle}
 		 </div>
{:/}

 9) data-sly-call : Use to call/invoke client library in your compoennet

 	Eg: 
{::nomarkdown}
data-sly-call="${clientlib.all @ categories='cq:jquery'}"
{:/}