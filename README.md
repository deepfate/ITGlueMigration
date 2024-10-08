# ITGlueMigration
Repo for notes regarding migration of archived ITGlue docs into proper folders in SharePoint.

Flow Pseudocode
- Get Reference Table from Excel Sheet
- For Each Row in Table,
  - Will be using 2 fields from each row:
    - Organization - To find our destination folder
    - Locator - To find the target folder to copy
  - Find Target Folder to copy using Locator.
  - Find Destination Folder using Organization
    - If Destination not found, copy Target Folder to "To Review" folder
    - Else, copy Target Folder to Destination using Organization
  - Proceed to next row

Actual Flow
- Manually Trigger A Flow
- Post message in chat notifying of flow start
- List rows present in Table. Now we have a table with a "Locator" column and a "Organization" column.
- List Folders in Solus LLC > Shared Docs > Customer Docs. This should allow us to search for destination folder more easily.
- For each row in table,
      - Find the folder to move using the "locator" field.
      - Move that folder to it's destination using the "organization" field
  
