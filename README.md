 # 🕊 mazeworldwide.db v1.0.1
- Fast Database Module
## 😏 Some Of Features
- Multiple Json Files
- Simple And Easy To Get Started
- Backup System
##  Getting Started
- You can start install the package on your project:
```
npm i mazeworldwide.db
```
- Then Start define it like this:
```javascript
const { Database } = require('mazeworldwide.db')
const db = new Database(/* db.json */)
```
- Or in typescript
```ts
import { Database } from 'mazeworldwide.db';
const db = new Database();
```

##  Some Notes 
- For the Database class, you can pass in a parameter to set a file rather than using the default file! 
- If the file dosen't exist, it will create it
- Path automatically set to **./**

## 🔋 Examples
- some exmaples
```javascript
const { Database } = require('mazeworldwide.db');
const db = new Database(/* db.json */)

// Set / Push Functions Examples
var object1 = {key: true, key2: "true"}
db.set('Object', object1); /* Object: {key: "value1", key2: "value2"} */

var array1 = ['element', 'element2']
db.set('Array', array1); /* Array: ['element', 'element2'] */
db.push('Array', 'element3'); /* Array: ['element', 'element2', 'element3'] */

// Object & Array Fetch
db.objectFetch('Object', 'key'); /* key: "value1" */
db.arrayFetch('Array', 1); /* element2 */

// Fetch / Get Functions
db.fetch('data'); // Fetches the value of the data
db.get('data'); // Get the value of the data
db.fetchAll(); // Fetches all the data in the database
db.all(); // Fetches everything in the database

// Remove / Delete Functions
db.remove('data'); // Removes the data from the database
db.delete('Array', 'element3'); // Removing something from an array using value/index
db.deleteKey('object', 'key'); // Deletes the provided key from the given object
db.deleteEach('data'); // Deletes each data that starts with the given parameter

// Clear / Destroy Functions
db.clear(); // Clears everything from the database
db.destroy(); // Delete the database file (And Clear All Data)

// Boolean Functions
db.has('data'); // Returns "true" or "false" if the database has the data or not.

// Maths Functions
db.add('data', 1); // Adds one to the data
db.subtract('data', 1); // Subtracts one from the data
db.math("eco", "+", 10); // Adds 10 to the data (without set it), You Can Use [+,-,*,/]
```
