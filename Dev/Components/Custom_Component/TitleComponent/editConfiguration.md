#Editconfig in AEM

- cq:editConfig is a node of type cq:editConfig.
- It defines the edit properties of a component. It enables component to appear in the sidekick or siderail. It is used to configure how a component is edited.

You can use editconfig for below fuctanality:

1) In-place editing.
2) Drag and drop.
3) Refresh a page after an author action.

## In-place editing

- It makes component to be editable in-line rather than dialog box.

- Within title component, create node of name: cq:editConfig and type: cq:EditConfig. Now right click on the cq:editConfig node and create node of name cq:inplaceEditing and type:cq:InplaceEditingConfig.
   
   Right Click - cq:editConfig > New Node > Name cq:inplaceEditing && type:cq:InplaceEditingConfig

- Add 2 properties on cq:inplaceEditing node. 
   active - boolean - true 
   editorType - string - title

- Create node on cq:InplaceEditing node of name config and type nt:unstructured. 

- Now if you click on title component you will see pencil icon using which you can edit component even without opening dialog.
