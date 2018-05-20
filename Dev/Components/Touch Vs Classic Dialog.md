# Touch Vs Classic Dialog:

 - Touch dialog and class dialog box in AEM
 - Dialog are small windows that are used to edit content and take input from the user.

There  are 2 types of dialog box in AEM. 

1. Touch optimized dialog box.
2. Classic dialog box.

## Classic dialog box : 
- It is based on ExtJs. 
- It is not responsive.
- dialog is the root node in classic dialog box.
- For input fields, xTypes property is used.
  Ex: xtype : textfield
- You can search for widget API for finding the list of fields you can use in classic dialog box.

## Touch optiomized dialog box:
- Based on Granitejs.
- It is responsive and works well with mobile, desktop and tablet.
- cq:dialog is the root node.
- For input fields, sling:resourceType property is used here.
   Ex: sling:resourceType : granite/ui/components/foundation/form/textfield
- You can find all list of fields in libs/granite/ui/components/foundation/form path.
