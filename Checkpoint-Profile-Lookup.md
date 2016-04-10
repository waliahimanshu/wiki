# Checkpoint: Profile Lookup

***Instructions***

We have an array of objects representing different people in our contacts lists.

A **lookUp** function that takes **firstName** and a property (**prop**) as arguments has been pre-written for you.

The function should check if **firstName** is an actual contact's **firstName** and the given property (**prop**) is a property of that contact.

If both are true, then return the "value" of that property.

If **firstName** does not correspond to any contacts then return **"No such contact"**

If **prop** does not correspond to any valid properties then return **"No such property"**

Remember to use [ Read-Search-Ask](How-to-get-help-when-you-get-stuck) if you get stuck. Try to pair program. Write your own code.

## Useful Links
- [Challenge: Accessing Objects Properties with Bracket Notation](http://www.freecodecamp.com/challenges/accessing-objects-properties-with-bracket-notation)
- [Challenge: Iterate with JavaScript For Loops](http://www.freecodecamp.com/challenges/iterate-with-javascript-for-loops)

## Problem Explanation:
- Change the code below `// Only change code below this line` and up to `// Only change code above this line`
- Take note that you are editing the inside of the `lookUpProfile` function
  - This function includes two parameters, `firstName` and `prop`
- The function should check look through the `contact` list for the given `firstName` parameter
  - If there is a match found, the function should then look for the given `prop` parameter
  - If both `firstName` and the associated `prop` are found, you should return the value of the `prop`
  - If `firstName` is found and no associated `prop` is found, you should return `"No such property"`
  - If `firstName` isn't found anywhere, you should return `"No such contact"`

## Hint: 1
- Use a **for loop** to cycle through the `contact` list

## Hint: 2
- Use a nested `if` statement to first check if the `firstName` matches, and then checks if the `prop` matches

## Hint: 3
- Leave your `return "No such contact"` out of the `for loop` as a final catch-all

## Spoiler Alert!
[![687474703a2f2f7777772e796f75726472756d2e636f6d2f796f75726472756d2f696d616765732f323030372f31302f31302f7265645f7761726e696e675f7369676e5f322e676966.gif](https://files.gitter.im/FreeCodeCamp/Wiki/nlOm/thumb/687474703a2f2f7777772e796f75726472756d2e636f6d2f796f75726472756d2f696d616765732f323030372f31302f31302f7265645f7761726e696e675f7369676e5f322e676966.gif)](https://files.gitter.im/FreeCodeCamp/Wiki/nlOm/687474703a2f2f7777772e796f75726472756d2e636f6d2f796f75726472756d2f696d616765732f323030372f31302f31302f7265645f7761726e696e675f7369676e5f322e676966.gif)

**Solution ahead!**

## Code Solution:

```
for (var x = 0; x < contacts.length; x++){
    if (contacts[x].firstName === firstName) {
        if (contacts[x][prop]) {
            return contacts[x][prop];
        } else {
            return "No such property";
        }
    }
}
return "No such contact";
```

# Code Explanation:
- The **for loop** runs, starting at the first object in the `contacts` list
- If the `firstName` parameter passed into the function matches the value of the `"firstName"` key in the first object, the `if` statement passes
- Then, if the `prop` parameter passed into the function is present in that object, the value of the `prop` is returned
  - If the second `if` statement fails, `"No such property"` is returned
- If the first `if` statement fails, the **for loop** continues on to the next object in the `contact` list
- If the `firstName` parameter isn't matched by the final `contact` object, the **for loop** exits and `"No such contact"` is returned

***Example Run***

- `lookUpProfile("Akira","likes");` runs
- `"Akira"` is matched to the `"firstName"` key in the first object, so the `if` statement returns true
- `"likes"` is found within the first object, so the second `if` statement returns true
- The value of `"likes"` is returned - `"Pizza", "Coding", "Brownie Points"`



# Credits:
If you found this page useful, you can give thanks by copying and pasting this on the main chat:  **`thanks @leftynaut for your help with Checkpoint: Profile Lookup`**

> **NOTE:** Please add your username only if you have added any **relevant main contents** to the wiki page. (Please don't remove any existing usernames.)
