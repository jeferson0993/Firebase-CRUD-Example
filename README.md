Live Demo http://earthchie.com/firebase/crud/

#### Rules
```json
{
  "rules": {
    ".read": true,
    ".write": "auth != null",
    
    "Entry":{
    	".read": true,
    	".write": "auth != null",
        
        "$child": {
            ".read": true,
            ".write": "newData.hasChildren(['views']) || auth != null"
        }
    }
      
  }
}
```
