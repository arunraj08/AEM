# Custom Component
 
 - Create a title component in AEM.

 - In this demo we have created title component first.
     a) Navigate to component content path (i.e. training > components > content )
     b) Right click > Create Component 
     c) Enter details of component 
     d) Rename jsp to html extension 

 - Then create a helper file which is a javascript helper class to write our business logic. 
     Ex: title.js provides business logic

 - Use this helper in title.html and used data-sly-use sightly attribute to read object.
    ```html  
    <h1 data-sly-use.title="title.js">${title.text}</h1>
    ```
 - Now include this title component in the body.html by replacing the title component placeholder using data-sly-resource attribute.

	```html 
	  <div class="we-Header" data-sly-resource="${'title' @ resourceType='training/components/content/title'}"></div>
	```

# Create Touch Dialog Box
  Create a touch dialog box for the Title component in AEM. This dialog box make it editable or authorable for the author.

 - Go to the title component, now copy the touch dialog(cq:dialog) from the foundation title component and paste in our title component. 
   AEM Path : /libs/wcm/foundation/components/title/cq:dialog
   Ex- Custom Comp Path: /apps/training/components/content/title/cq:dialog

 - Rename custom component title.
   Ex: jcr:title : We Train Title

 - Optional : If some node are not required from OOB. Delete the type node as it's not needed. 

 - Notice the fielLablel, fieldDescription, name and sling:resourceType property. Dialog won't appear if we don't have cq:editConfig node. So, create this node and now you can edit title component.

## Make Component Authorable

   By default dialog wont appear when cq:editConfig node is not available for the component. This node requires to be created to make component editable.

 - Create cq:editConfig Node under the component.

   RightClick > Create Node > Name : cq:EditConfig && Type : cq:EditConfig
   
 - Make sure editConfig created under component node.

    Path : /apps/training/components/content/title/cq:editConfig

 - Validate compoenent is editable through EditMode.

 - Once custom title component values are modifed and saved, custom component title jcr:node will be created under jcr:content for the page.

   Ex: /content/we-train/en/products/jcr:content/title
       jcr:title > New product Page title
