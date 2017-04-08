# ElasticSearch FollowUp Plugin 

The plugin tracks CRUD changes made in an ElasticSearch index.

## Installation

Target folder contains compiled binaries ready for use. The first 3 numbers of the version tag refers to the version of ElasticSearch the plugin built for.

* ElasticSearch 5.2.2

``` bash
elasticsearch-plugin install   https://github.com/artcomventure/elasticsearch-followup-plugin/raw/master/target/elasticsearch-followup-plugin-5.2.2.1.zip
``` bash

* ElasticSearch 2.4.1

``` bash
plugin install https://github.com/artcomventure/elasticsearch-followup-plugin/raw/master/target/elasticsearch-followup-plugin-2.4.1.2.zip
```

* ElasticSearch 2.4.0

``` bash
plugin install https://github.com/artcomventure/elasticsearch-followup-plugin/raw/master/target/elasticsearch-followup-plugin-2.4.0.2.zip
```

* ElasticSearch 2.3.5

``` bash
plugin install https://github.com/artcomventure/elasticsearch-followup-plugin/raw/master/target/elasticsearch-followup-plugin-2.3.5.1.zip
```

* ElasticSearch 1.4.4

``` bash
plugin -u https://github.com/artcomventure/elasticsearch-followup-plugin/raw/master/target/elasticsearch-followup-plugin-1.4.4.2.zip -i followup
```


Restart ElasticSearch.

## Usage

Track changes in myindex:

```
http://localhost:9200/myindex/_followup?start
```

Get changes:

```
http://localhost:9200/myindex/_followup
```

Stop tracking: 

```
http://localhost:9200/myindex/_followup?stop
```

Clear changes: 

```
http://localhost:9200/myindex/_followup?clear
```

The tracking buffer is only limited by heap size, don't forget to turn it off. :)
