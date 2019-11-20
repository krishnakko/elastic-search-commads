{
  "template": "levelone_*",
  "version" : 1,
  "settings" : {
    "index.refresh_interval" : "5s",
    "index.number_of_replicas": 2,
    "index.number_of_shards": "5"
  },
  "mappings" : {
        "properties": {
          "UUID": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Url": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Source": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Author": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Title": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Content": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "ImageUrl": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "PublishedDate": {
            "type" : "date"
          },
          "FRE": {
            "type": "float"
          },
          "SIS": {
            "type": "float"
          },
          "FKG": {
            "type": "float"
          },
          "CLIS": {
            "type": "float"
          },
          "ARI": {
            "type": "float"
          },
          "DCRS": {
            "type": "float"
          },
          "DW": {
            "type": "long"
          },
          "LWF": {
            "type": "float"
          },
          "GF": {
            "type": "float"
          },
          "TS": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Words_Count": {
            "type": "long"
          },
          "Cleaned_Words_Count": {
            "type": "long"
          },
          "Category": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Country": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Level": {
               "type": "integer"
                }
          
        }
    }
  }




PUT _template/levelone_temp
{
  "index_patterns":["levelone_*"],
  "settings":{
    "index.refresh_interval" : "5s",
    "index.number_of_replicas": 2,
    "index.number_of_shards": 3
  },
  "mappings" : {
        "properties": {
          "UUID": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Url": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Source": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Author": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Title": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Content": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "ImageUrl": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "PublishedDate": {
            "type" : "date"
          },
          "FRE": {
            "type": "float"
          },
          "SIS": {
            "type": "float"
          },
          "FKG": {
            "type": "float"
          },
          "CLIS": {
            "type": "float"
          },
          "ARI": {
            "type": "float"
          },
          "DCRS": {
            "type": "float"
          },
          "DW": {
            "type": "long"
          },
          "LWF": {
            "type": "float"
          },
          "GF": {
            "type": "float"
          },
          "TS": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Words_Count": {
            "type": "long"
          },
          "Cleaned_Words_Count": {
            "type": "long"
          },
          "Category": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Country": {
            "type": "text",
            "fields": {
              "keyword": {
                "type": "keyword",
                "ignore_above": 256
              }
            }
          },
          "Level": {
               "type": "integer"
                }
          
        }
    }
}
