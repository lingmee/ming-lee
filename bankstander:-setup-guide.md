### Quick Links

[Use Item (Herb Cleaning)](https://github.com/Elli-tt/el-plugins/wiki/bankstander:-setup-guide#use-item)

[Use Item On Item (Potion Making)](https://github.com/Elli-tt/el-plugins/wiki/bankstander:-setup-guide#use-item-on-item)

[Use Tool On Item (Fletching)](https://github.com/Elli-tt/el-plugins/wiki/bankstander:-setup-guide#use-tool-on-item)

[Useful Explanations](https://github.com/Elli-tt/el-plugins/wiki/bankstander:-setup-guide#useful-explanations)

## General

**Client:**
* Make sure you are in resizable mode.

![](https://cdn.discordapp.com/attachments/767454775246848010/767454786705555526/unknown.png)

**Location:**
* Make sure you are near a bank booth. Grand exchange is supported.

![](https://cdn.discordapp.com/attachments/767454775246848010/767454951345356820/unknown.png)

**Hints and Tips:**
* If a config option is not mentioned in this guide. Assume that the value can be anything. For example, for **Herb Cleaning**, you only need to set two config options: **First Item ID** and **Inventory OpCode**. All of the **other** options can be random or 0. The exception to this rule is **Placeholder ID**.

![](https://cdn.discordapp.com/attachments/767454775246848010/767455422046928896/unknown.png)

## Use Item 
This option can be used for bank standing activities that require the player to simply click each item in their inventory individually.

An example of this is **Cleaning Herbs**.

**Config options:**
* **First Item ID:** ID of the Grimy Herb you would like to clean. (207 - Grimy Ranarr Weed)
* **Inventory OpCode:** 33

![](https://cdn.discordapp.com/attachments/767454775246848010/767456364020498522/unknown.png)

**Bank setup:**
* Make sure your bank contains the grimy herb you would like to clean.

**Inventory setup:**
* Start with an empty inventory or an inventory filled with the grimy herb you want to clean.

## Use Item On Item
This option can be used for bank standing activities that require the player to use an item on another item.

An example of this is **Potion Making**.

**Config options:**
* **First Item ID:** Unfinished Potion or Secondary Ingredient Id (99 - Ranarr potion (unf))
* **Second Item ID:** Secondary Ingredient or Unfinished Potion Id (231 - Snape grass)
* **Menu OpCode:** 57
* **Menu Param1:** 17694734

![](https://cdn.discordapp.com/attachments/767454775246848010/767456244251361331/unknown.png)

**Bank setup:**
* Make sure your bank contains enough of the unfinished potion and secondary ingredient.

**Inventory setup:**
* Start with an empty inventory or an inventory filled with 14 unfinished potions and 14 secondary ingredients.

![](https://cdn.discordapp.com/attachments/767454775246848010/767457606067290152/unknown.png)

## Use Tool On Item
This option can be used for bank standing activities that require the player to use a tool on another item.

An example of this is **Fletching**.

**Config options:**
* **First Item ID:** Log Id (1521 - Oak logs)
* **Second Item ID:** Tool Id (946 - Knife)
* **Menu OpCode:** 57
* **Menu Param1:** 17694734 (Shaft), 17694735 (Shortbow), 17694736 (Longbow).

![](https://cdn.discordapp.com/attachments/767454775246848010/767459249487347753/unknown.png)

**Bank setup:**
* Make sure your bank contains logs and a knife (if not already in your inventory.

**Inventory setup:**
* Start with an empty inventory or with a knife and the rest filled with the logs you would like to fletch.

![](https://cdn.discordapp.com/attachments/767454775246848010/767459690262560788/unknown.png)

## Useful Explanations

**Inventory OpCode**

An inventory OpCode is a number that represents the menu option that is clicked for the Use Item portion of the plugin. The reason we have to customise this value is so that we get the appropriate action when we left click on the items. For example, OpCode 33 tells the plugin that you want to use the 'Clean' menu option when it left clicks on grimy herbs in your inventory.

Use Oak logs has an OpCode of 38.

![](https://cdn.discordapp.com/attachments/767454775246848010/767461778279759932/unknown.png)

Drop Oak logs has an OpCode of 37.

![](https://cdn.discordapp.com/attachments/767454775246848010/767462005896380436/unknown.png)

**Menu OpCode**

Similarly, menu opcode is a number that represents the menu option that is clicked for the Use Item on Item and Use Tool On Item portions of the plugin. Again, we customise this number so that we get the appropriate action when we interact with the menu. The Make Oak shield menu entry has an OpCode of 57.

![](https://cdn.discordapp.com/attachments/767454775246848010/767464024165318736/unknown.png)

**Menu Param1**

In this plugin the menu OpCode represents which option is clicked in the Multi Skill menu. An update from Jagex combined all old interfaces into this new Multi Skill menu, therefore instead of supporting many different menus, we support this one type of menu and change the Menu OpCode accordingly.

An example of the multi skill menu for fletching an oak log.
The options start at value: 17694734 for arrow shafts (space) and increase by one for each other option ending at 17694734+4 = 17694738 for the shield (5).

![](https://cdn.discordapp.com/attachments/767454775246848010/767463308814450708/unknown.png)

**Placeholder ID**

Placeholder IDs were added to enable bank standing activities such as crafting d'hide bodies. Since you need a needle and a thread to craft dragonleather, this leaves you with 26 free inventory spaces. A d'hide body takes 3 dragonleather to craft, 26/3=8.66666667. Therefore, in order to ensure that the plugin 'runs out' of dragonleather every inventory we add two random items to our inventory. This leads to us having 24 free spaces, 24/3=8, a nice whole number.

An example inventory for crafting green dragonhide bodies, including two random placeholder items.

![](https://cdn.discordapp.com/attachments/767454775246848010/769995400463122482/unknown.png)

As you can see in the settings we use first item id as green dragon leather (1745), tool id as needle (1733), placeholder id #1 as thread (1734), and our two extra placeholder ids #2 and #3 as logs (1511) and oak logs (1521) respectively.

The menu opcode stays at 57, and the menu param1 at 17694734.

![](https://cdn.discordapp.com/attachments/767454775246848010/769995441172774932/unknown.png)