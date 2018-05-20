# Design dialog and difference in dialog and design dialog

Lets see what is design dialog, when to use it and difference between dialog and design dialog.

Design dialog is a dialog which allows to store content/configurations that can be accessed across pages. When we require component whose component should be same throughout the application which are created using same template. Example logo, header, navigation etc.

And changes which are made through the design dialog will get reflected across all the pages created using the same template.

# Difference

Node : In Design dialog, node name is design_dialog.
       In dialog, node name is dialog.

Storage: In design dialog, content will be stored in etc/design path.
         In dialog, content will be stored in the content/website.

Mode: Design dialog opens in the design mode.
      Dialog opens in the edit mode.

Object: currentStyle object is used to read content in design dialog.
        Properties object is used to read content in dialog.

Availability: Design Dialog - No touch ui version is available till aem 6.2
              Dialog - Touch ui dialog is available from aem 6.0
