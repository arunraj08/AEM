# Create a design dialog in AEM. 

- We will create a design dialog for the tile component. We will create drop down on it from which we will change the style which will be reflected across all the pages using the same template. 

- Creating desing dialog is same as creating classic dialog box only name should be design_dialog.

## Steps:

1) Right Click Component > Create Design Dialog. 
   
   Name : design_dialog
   Title : Design Dialaog

2) Navigate to the tabs Node.
    
    Path : /apps/training/components/content/title/design_dialog/items/items/tab1

3) Create New node with Type as cq:WidgetCollection
    
    Name : items
    Type : cq:WidgetCollection

4) Create child node with Type as cq:Widget
    
    Name : type (It can be any name)
    Type : cq:Widget

5) Create properties for child Node
    
    | Name        | Type           | Value  |
	| ------------- |:-------------:| -----:|
	|fieldLabel     | String        | Type |
	| name      | String      |   ./type |
	|type     | String        | select |
	| xtype      | String      |   selection |
	| defaultValue      | String      |   h1 |

6) Create new node under child node (i.e type) of cq:WidgetCollection Type
   
   Name : options
   Type :  cq:WidgetCollection 

7) Create Four node for storing the collection values.
    
    Node Name : h1
    Type: nt:unstructured

    Properties:
    | Name        | Type           | Value  |
	| ------------- |:-------------:| -----:|
	|text     | String        | H1 |
	|value     | String        | h1 |

8) Repeat same step for h2,h3,h4.

