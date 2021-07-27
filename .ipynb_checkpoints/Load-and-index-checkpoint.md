



## Mappings:
Before loading data mappings must be set up. Mappings divide the documents in the index into logical groups and specify the characteristics of the fields. 
 
 
  
## Load data:

`Invoke-RestMethod "http://localhost:9200/shakespeare/doc/_bulk?pretty" -Method Post -ContentType 'application/x-ndjson' -InFile "shakespeare_6.0.json"`

## Queries

HEAD harvardmetadata



GET /harvardmetadata/_search?q="https://doi.org/10.11588/data/0HJAJS"

GET /harvardmetadata/_search?q="https://doi.org/10.11588/data/0HJW2A"

GET /harvardmetadata/_search
{
  "query": {
    "match": {
      "identifier": "https://doi.org/10.11588/data/0HJW2A"      
      
      }
    }
  }

GET /harvardmetadata/_search
{
  "query": {
    "query_string": {
      "default_field": "@id",
      "query": "https://doi.org/10.11588/data/0HJW2A"
    }
  }
}


POST /schools/_search
{
   "query":{
      "match_all":{}
   }
}