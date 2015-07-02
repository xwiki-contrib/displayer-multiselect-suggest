displayer-multiselect-suggest
=============================

[![XWiki labs logo](https://labs.xwiki.com/xwiki/bin/download/Developments/Xlabs/xwiki-labs-project.png "XWiki labs")](https://labs.xwiki.com/xwiki/bin/view/Main/WebHome)
##Description
A custom suggest displayer for DBList object properties which adapts the suggest feature to multiple selection.

##Usage
* To activate it, you must edit the XClass and set, for the target property, the fields Use suggest and Multiple select to true, and the field Custom display to:
{{include document="XWiki.SuggestDisplay" /}}

* To activate the itemsEditable mode that allows you to create new items and edit selected items, keep the configuration above and precede the {{include}} macro with below code.

```
{{velocity}}
#set($SuggestDisplayItemsEditable = true)
{{/velocity}}
```
* To force the space where the new items will be created to a custom space add the below code before the {{include}} macro.

`#set($SuggestDisplayEditModeSpace = "yourSpace")`

Notice that the default space of new items is the space of the document that calls the displayer-multiselect-suggest. 
