#Rich text editor in touch UI dialog in AEM:
 
I have covered how you can add rich text editory in touch ui dialog in aem.

Rich text editor provides several features such as:
 - bold
 - italic
 - underline
 - list
 - alignment
 - find and replace
 - subscript and superscript
 - spell check
 - etc.

## Create RichText Field

- In this demo I will replace textfield in title component dialog with the rich text editor. To make rich text editor work first open the chrome://flags in the new tab in chrome browser. Disable the toch event api then only it will work.

- In order to make field type as RichText. Assign sling:resourceType to cq/gui/components/authoring/dialog/richtext and now copy the rtePlugins and uiSetting from the foundation text component this process is called overlaying.
 
  AEM Path for Text: /libs/foundation/components/text/cq:dialog/content/items/text/items/column/items/text

- Make sure rtePlugin and uisetting are copied properly under the component node.
  
  EX: /apps/training/components/content/title/cq:dialog/content/items/column/items/title/rtePlugins
      /apps/training/components/content/title/cq:dialog/content/items/column/items/title/uiSettings

- Make Rich Text works on in-place Editing
   
   a) Make Editor Type as text.
   b) Copy rtePlugins from OOB component and paste it under custom editConfiguration.
     Path: /apps/training/components/content/title/cq:editConfig/cq:inplaceEditing/config/rtePlugins

- Now open the title component, you can see the options has been enabled now for rich text. But saving the text will add the html tabs over there. 

- To resolve inline HTML issue. Assign context to html.
  ```html
  <h1 data-sly-use.title="title.js">${title.text @context='html'}</h1>
  ```

## Additional Features 

### Find, Replace , Subscript and SuperSscript

  Adding find, replace, subscript and subscript functionality in Rich text editor of AEM

- Create 2 nodes findreplace and subsuperscript node with nt:unstructured type and add properties features as * to enable all features.
 
  Path : /apps/training/components/content/title/cq:dialog/content/items/column/items/title/rtePlugins/findreplace
         /apps/training/components/content/title/cq:dialog/content/items/column/items/title/rtePlugins/subsuperscript

-  Add Properties features as * to enable all features. This attribtes needs to be created under both plugins (i.e. findreplace, subsuperscipt)

-  Now go to uisettings, cui and inline and in the properties window select the value of toolbar and add findreplace#find, findreplace#replace, subsuperscript#subscript and subsuperscript#superscript values and save it.

- Now if you open the touch ui dialog you can see on the toolbar these 4 functionalies are available for use.

### Spell Check
Adding Spell check functionlity in rich text editor of AEM

- To add spell check in rte, go to cq:dialog of title component and find out the rtePlugins node.
- create a node spellcheck of type nt:unstructured and property features as *.
- Now go to the uiSettings, cui, inline node. And now add value in the toolbar property of inline node. Add spellcheck#checktex value and save it.

## Debug :

1) In AEM 6.2 & 6.3, You might face issue with Rt plugins (i.e Rich Text Editor). Touch Events API needs to be disabled in chrome.
   
   *Steps:*
    a) Navigate to chrome://flags
    b) Disable Touch Events API
