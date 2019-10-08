&nbsp;
# -FAMLOG-
&nbsp;

&nbsp;

&nbsp;

CS157A - Section 01

Team 39

&nbsp;

&nbsp;

*Benjamin Wen Shen Lee*

*Grace To*

*Jeffrey Nguyen*

&nbsp;

&nbsp;

&nbsp;

# Project Design & DB Design

&nbsp;

## -FamLog- 
&nbsp;

For our project, we are building an application that will allow households to maintain a
centralized shopping list, based on the separate personal lists created by individuals of the
household.

## E/R Diagram
&nbsp;

![E/R Diagram](https://github.com/CS157A-Team39-FAMLOG/project_design/blob/master/Team39ERD.png)
						
							E/R Diagram 
&emsp;
## Descriptions
Through our application, any individual can create an *Account* with a unique
*accountName* and a password for the respective household. *Users* are then created within the
*Account*, representing the different individuals within that household.

Each of the *Users* will have a unique *name*. Every one of the *Users* also has exactly one
*PersonalList* which is identified by a unique *userID*.

The entity *PersonalList* also contains the attribute *itemName*, the *quantity* requested, the
*priority* of each item, and the attribute *notes*. This is representative of the individual shopping
list, held by each of the *Users* of a household.

By default, the *Account* has exactly one *PurchaseHistory*, and each PurchaseHistory
belongs to exactly one *Account*. Attributes of *PurchaseHistory* include the *buyer* of the item,
the attribute *itemName*, the *date* of purchase, the *price* of each item, the *quantity* of the items
bought, and the attribute *belongsTo*, which represents to whom’s list the *Item* belongs to.