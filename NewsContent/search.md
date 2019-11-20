# First we have to create ins=dexes and have to give correct mapping

# To get all the records in levelone
GET /levelone/_search?q=*  

# with Name
GET /levelone/_search?q=Author:PerthNow

# Title search query
GET /levelone/_search?q=Title:<searching>
GET /levelone/_search
{
  "query": {  
    "match": {
      "Title": "Australia"
    }
  }
}

# For Title and Content We have to include both text type and keyword type
# Example
In mapping

"Title":{
    "type":"text",
    "fields":{
        "keyword":{
            "type":"keyword"
        }
    }
}
"Content":{
    "type":"text",
    "fields":{
        "keyword":{
            "type":"keyword"
        }
    }
}

# Multiple Search Conditions
GET /levelone/_search?q=PublishedDate:2019-11-05 AND Author:PerthNow

curl -XGET "http://localhost:9200/levelone/_search?q=PublishedDate:2019-11-05 AND Author:PerthNow"


GET /levelone/_search?q=Level:1 AND Category:science AND Country:in

GET /levelone/_search
{
  "query": {
    "bool": {
      "must": [{
           "term": {
             "Level": 1
           }
         },
         {
           "term": {
             "Country": "au"
           }
         },
         {
           "term": {
             "Category": "science"
           }
         }
      ]
    }
  }
}

curl -XGET "http://localhost:9200/levelone/_search" -H 'Content-Type: application/json' -d'{  "query": {    "bool": {      "must": [{           "term": {             "Level": 1           }         },         {           "term": {             "Country": "au"           }         },         {           "term": {             "Category": "science"           }         }      ]    }  }}'