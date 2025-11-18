# Favorite

## Image
![screenshot of sample](./assets/favorite-add.png)  
![screenshot of sample](./assets/favorite-remove.png)

## Summary
Add a list item or file as a favorite.

When the button is pressed the currently logged in user will be added/remove to a multi people field

## Requirements
* The user must have edit/write privilege

## Column Types
- Multi people

## How To
**Setup**

1. Create a new **person** column. Don't use any spaces or special characters to retain a good internal name (_you can rename the column afterwards_)
2. In **advanced** select **Allow multiple selections**
3. In the [favorite.json](./favorite.json) replace **Favorite** with the internal name of your column. Note that **Favorite** must be replaced in 2 places (line 19 & 52)

```
      "customRowAction": {
        "action": "setValue",
        "actionInput": {
          "Favorite": "=appendTo(@currentField.email , @me)"
        }
```