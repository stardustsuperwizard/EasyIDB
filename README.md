# EasyIDB
 Simple API wrapper for interacting with IndexedDB

# How to use:
To use the library, instantiate the class:
```javascript
tables = [
    {
        'name': 'Table1',
        'options': {
            autoIncrement: true,
            keyPath: 'id'
        }
    },
    {
        'name': 'Table2',
        'options': {
            autoIncrement: true,
            keyPath: 'id'
        }
    },
    {
        'name': 'Table3',
        'options': {
            autoIncrement: true,
            keyPath: 'id'
        }
    }
]
const idb = new EasyIDB('mainDB', tables, 1);
idb.getDB();
```

Entries can then be added to tables (ObjectStores):
```javascript
idb.createEntry('Table1', {'Statement': 'Hello World'})
```

Entries can be deleted by KeyPath:
```javascript
ibd.deleteEntry('Table1', 1)
```


 # Credits
 Based off of the following tutorial: https://www.raymondcamden.com/2019/10/16/using-indexeddb-with-vuejs

 This Stack Excahnge: https://stackoverflow.com/questions/44002460/getting-object-store-already-exists-inside-onupgradeneeded

 And this one too: https://stackoverflow.com/questions/24382085/failed-to-execute-createobjectstore-on-idbdatabase#24402107
 