# Elasticsearch

Elasticsearch là search enginer hoạt động độc lập như memcached.
Tìm hiểu về Elasticsearch 


## Install ES on mac

#### 1. Install

```
$brew install elasticsearch
```

Start

```
elasticsearch --config=/usr/local/opt/elasticsearch/config/elasticsearch.yml
```

Verify config:

```
curl -X GET http://localhost:9200
```

```
	{
	  "status" : 200,
	  "name" : "Silvermane",
	  "version" : {
	    "number" : "1.1.0",
	    "build_hash" : "2181e113dea80b4a9e31e58e9686658a2d46e363",
	    "build_timestamp" : "2014-03-25T15:59:51Z",
	    "build_snapshot" : false,
	    "lucene_version" : "4.7"
	  },
	  "tagline" : "You Know, for Search"
	}
```

#### 2. Install plugin

Install Head

Check where elasticsearch installed

```
curl "localhost:9200/_nodes?pretty=true&settings=true"
```

Result: find home

```
"path" : {
          "data" : "/usr/local/var/elasticsearch/",
          "home" : "/usr/local/Cellar/elasticsearch/1.1.0",
          "plugins" : "/usr/local/var/lib/elasticsearch/plugins",
          "logs" : "/usr/local/var/log/elasticsearch"
        },
```

Move to elasticsearch home

```
cd /usr/local/Cellar/elasticsearch/1.1.0
```

Install 

```
bin/plugin --install mobz/elasticsearch-head
```

Open Head

```
open http://localhost:9200/_plugin/head/
```

## Completion suggest

http://www.elasticsearch.org/blog/you-complete-me/
Next time

## Search Japanese

http://engineer.wantedly.com/2014/02/25/elasticsearch-at-wantedly-1.html
Chú ý version của elasticsearch và kuromoji phải giống nhau.



