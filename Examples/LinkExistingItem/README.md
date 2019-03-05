# Link to existing Item

This example shows how to create link from one existing item to another. In other words, basic relation.

First we create array of relation criteria. We need to know GUIDs of two items we want to link an their respective foldernames. The word GENERAL in relation type means, that this will be basic relation, simple link between two items .
```c#

// Save Relation
wcfConnection.CallMethod("SaveRelation", JObject.FromObject(new
{
    transmitObject = new
    {
        ItemGUID1     = "129641b8-3677-11e7-9e49-080027cbca76",
        ItemGUID2     = "d9705ddc-9161-44e3-82cd-0bd0063b66f5",
        FolderName1   = "Projects",
        FolderName2   = "Contacts",
        RelationType  = "GENERAL"
    }
}));

```


## Output

In this example we took project with one already related contact.

![example output](Images/sample_output_before.PNG)

After executing the code, we should see the second contact in the contacts tab on project.

![example output](Images/sample_output_after.PNG)

## Sample code

To see the whole sample code click  [here](Program.cs)

## Folder name

To ease understanding folder names, look  [here](../../blob/master/FolderNames.md).