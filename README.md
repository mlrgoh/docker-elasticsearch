# Dockerfile Elasticsearch

## Install

- `docker build -t <namespace>/elasticsearch:2.1 .`

## Usage

To run an Elasticsearch node

```
docker run -t -i -p 9200:9200 <namespace>/elasticsearch:base /bin/bash
root@123456abcdef:/# service elasticsearch start
	* Starting Elasticsearch Server [ OK ]
Open a web browser and go to http://<hostname>:9200/
	{
	  "status" : 200,
	  "name" : "Techno",
	  "version" : {
		"number" : "1.1.1",
		"build_hash" : "f1585f096d3f3985e73456debdc1a0745f512bbc",
		"build_timestamp" : "2014-04-16T14:27:12Z",
		"build_snapshot" : false,
		"lucene_version" : "4.7"
	  },
	  "tagline" : "You Know, for Search"
	}
```