# Iris API using sklean
You can use this API by issue a json like the following 
```json
{
  "s1":1,
	"s2":0.2,
	"s3":0.4,
	"s4":0.3
}
```
Use it with *Post request* to the following endpont *'/clf'*

Example :
```bash
curl --location --request POST 'http://127.0.0.1:5000/clf' \
--header 'Content-Type: application/json' \
--data-raw '{
	"s1":1,
	"s2":0.2,
	"s3":0.4,
	"s4":0.3
}'
```
The result sould be :
```bash
{
  "confidences": {
    "0": 0.417,
    "1": 0.583,
    "2": 0.0
  },
  "prediction": 1,
  "response": "data successfully loaded",
  "status": "success"
}
```
