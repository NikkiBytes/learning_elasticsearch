
Load data:

`Invoke-RestMethod "http://localhost:9200/shakespeare/doc/_bulk?pretty" -Method Post -ContentType 'application/x-ndjson' -InFile "shakespeare_6.0.json"`


