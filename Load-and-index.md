



## Mappings:
Before loading data mappings must be set up. Mappings divide the documents in the index into logical groups and specify the characteristics of the fields. 
 
 
  
## Load data:

`Invoke-RestMethod "http://localhost:9200/shakespeare/doc/_bulk?pretty" -Method Post -ContentType 'application/x-ndjson' -InFile "shakespeare_6.0.json"`

