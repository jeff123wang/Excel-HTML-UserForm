# Excel-HTML-UserForm
using web technology to enhance excel vba userform

## 1/16/2025 update
* working on using "mutation Observer" to detect title change
* use title to pass data as JSON
* This could be wrapped later as a simple api and later use React UseEffect to get data

## 1/18/2025 update
mutation observer is moved from observing title change to "description" meta tag. 

Here is logic to grab data from Excel
1. Set up mutation observer to observe "description" meta tag in javascript
2. Change title to trigger VBA code in javascript
3. VBA will pass JSON data to "description" meta tag
4. Mutation observer call back will update table using JSON string found in "Description" meta tag
5. Mutation observer is disconnected, ready for a new operation. 

Here is logic to send bata back to Excel
1. Update Meta tag in javascript
2. Update title to notify VBA data is ready in javascript
3. Title change will trigger VBA titleChange event and get data from meta tag in VBA
