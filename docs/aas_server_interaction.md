# Basic interactions with AAS SERVER
Once deployed, you can access to the Swagger proposed by AAS Server on the link:

http://localhost:5001/swagger/index.html

Or you can directly access to the main page of the server using the link

http://localhost:5001

# Short guide
- Call for the AAS server to browse all AASs registered in this server:
    - GET http://localhost:5001/shells/$reference

- From the answer, get the "value" from the key "AssetAdministrationShell"
  ```json
  {  
  "result": [
      {
        "type": "ModelReference",
        "keys": [
          {
            "type": "AssetAdministrationShell",
            "value": "https://htw-berlin.de/ids/aas/demoaasv3"
          }
        ]
      }
    ]
  }
  ```
- Encode in base64 the value. In the example you will get: 
```
https://htw-berlin.de/ids/aas/demoaasv3 -> aHR0cHM6Ly9odHctYmVybGluLmRlL2lkcy9hYXMvZGVtb2Fhc3Yz 
```

- This will be the ID of the shell of the element that you can use in further endpoints, for example
  - GET http://localhost:5001/shells/aHR0cHM6Ly9odHctYmVybGluLmRlL2lkcy9hYXMvZGVtb2Fhc3Yz

- You can navigate through all the other options using the data from the above request 