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

![E/R Diagram](https://github.com/CS157A-Team39-FAMLOG/project_design/blob/master/ERD_final.png)
						
							E/R Diagram 
&emsp;
## Descriptions
Through our application, any individual can create an *Account* with a unique *accountName* and a
*password* for the respective household. A *User* is then created within the *Account*, representing
the different individuals within that household. 

Every *User* will have a unique *userID* and *name*. Each User also has exactly one *PersonalList* which
is identified by a unique *personalListID*. 

The entity *PersonalList* also contains the attributes which include the *quantity* requested, the *priority*
of each item, and the attribute *notes*. This is representative of the individual shopping list, held by
each *User* within a household.

*PersonalList* also has a relationship with the entity *Item*. *PersonalList* contains the *Item* that was 
chosen by the *User* to add to their list. *Item* has the attributes of *brand*, *itemName*, and the unique
attribute *itemID*. *Item* shares a relationship with *PurchaseHistory*. *PurchaseHistory* records the *Item*,
adding it to the rest of the purchase history. 	

By default, the *Account* has exactly one *PurchaseHistory*, and each *PurchaseHistory* belongs to exactly one *Account*.
This entity has the unique attribute *purchaseID*. Other attributes of *PurchaseHistory* include the *buyer* of the item,
the attribute *itemName*, the *date* of purchase, the *price* of each item, the *quantity* of the items bought, and the
attribute *belongsTo*, which represents to whom’s list the *Item* belongs to. 