<p align="center">
  <a href="https://manticoresearch.com" target="_blank" rel="noopener">
    <img src="https://manticoresearch.com/wp-content/uploads/2019/12/manticore-logo-central-M-1.png" width="140" alt="Manicore Search Logo">
  </a>
</p>

<h1 align="center">
  Manticore Search 3.4.0
</h1>

<h3 align="center">
  <a href="https://manticoresearch.com">Website</a> • 
  <a href="http://bit.ly/2Q9uGj4">Downloads</a> • 
  <a href="https://docs.manticoresearch.com">Docs</a> • 
  <a href="https://play.manticoresearch.com">Courses</a> • 
  <a href="https://forum.manticoresearch.com">Forum</a> • 
  <a href="https://slack.manticoresearch.com">Chat</a> • 
  <a href="https://twitter.com/manticoresearch">Twitter</a>
</h3>

<p>&nbsp;</p>

# Introduction
Manticore Search is a database designed specifically for search, including full-text search. What differs it from other solutions is:
* SQL-first: the native Manticore's syntax is SQL. It speaks SQL over HTTP and MySQL protocol (you can use your preferred mysql client)
* JSON over HTTP: to provide more programmatic way to manage your data and schemas Manticore provides HTTP JSON protocol. Very similar to the one from Elasticsearch
* Written fully in C++: starts fast, doesn't take much RAM, low-level optimizations give good performance
* Real-time inserts: after INSERT is made the document can be read immediately
* [Interactive courses](https://play.manticoresearch.com/) for easier learning
* Built-in replication and load balancing
* Can sync from MySQL/Postgresql/ODBC/xml/csv out of the box
* Not fully ACID-compliant, but supports transactions and binlog for safe writes

[Craigslist](https://www.craigslist.org/), [Socialgist](https://socialgist.com/), [PubChem](https://pubchem.ncbi.nlm.nih.gov/) and many others use Manticore for efficient searching and stream filtering.

# More features
* Full-text search and relevance:
  - Over 20 [full-text operators](https://play.manticoresearch.com/fulltextintro/) and over 20 ranking factors
  - Custom ranking
* Other search capabilities:
  - [Faceted search](https://play.manticoresearch.com/faceting/)
  - [Geo-spatial search](https://play.manticoresearch.com/geosearch/)
  - [Spell correction](https://play.manticoresearch.com/didyoumean/)
  - [Autocomplete](https://play.manticoresearch.com/simpleautocomplete/)
  - Wide range of functions for filtering and data manipulation
* NLP:
  - Stemming
  - Lemmatization
  - Stopwords
  - Synonyms
  - Wordforms
  - Advanced tokenization at character and word level
  - [Proper Chinese segmentation](https://play.manticoresearch.com/icu-chinese/)
  - [Text highlighting](https://play.manticoresearch.com/highlighting/)
* Stream filtering [using a "percolate" index](https://play.manticoresearch.com/pq/)
* High-availability:
  - Search index can be distributed across servers and data-centers
  - [Synchronous replication](https://play.manticoresearch.com/replication/)
  - Built-in load balancing
* Security:
  - [https support](https://play.manticoresearch.com/https/)
* Data types:
  - multiple in-memory numeric fields
  - in-memory "string" for fast filtering
  - on-disk "[stored](https://play.manticoresearch.com/docstore/)" for key-value purpose
  - JSON
  - multi-value attribute

# Installation

### Docker
Docker image is available on [Docker Hub](https://dockr.ly/33biV0U).

To play with Manticore Search in Docker just run:

```
docker run --name manticore --rm -d manticoresearch/manticore && docker exec -it manticore mysql -w && docker stop manticore
```

When you exit from the mysql client it stops and removes the container, so use it only for testing / sandboxing purposes. 

The image comes with a sample index which can be loaded like this:

```
mysql> source /sandbox.sql
```

Also the mysql client has in history several sample queries that you can run on the above index, just use Up/Down keys in the client to see and run them.

Read [the full instruction for the docker image](https://dockr.ly/33biV0U) for more details.

### Packages

## [Ubuntu, Debian, Centos, Windows and MacOS packages are here](https://www.manticoresearch.com/downloads).

### YUM repo for RHEL/Centos
```
yum install https://repo.manticoresearch.com/manticore-repo.noarch.rpm
yum install manticore
```

### Homebrew on MacOS
```
brew install manticoresearch
```

### Windows
See [instruction here](https://docs.manticoresearch.com/latest/html/installation.html#installing-manticore-on-windows).

### MacOS .dmg
See [instruction here](https://docs.manticoresearch.com/latest/html/installation.html#installing-manticore-on-macos).


# Documentation and community channels

  * [Interactive courses](https://play.manticoresearch.com)
  * [Documentation](https://docs.manticoresearch.com)
  * [Manticore Community Forum](https://forum.manticoresearch.com/)
  * [Public Slack chat](http://slack.manticoresearch.com/)
  * [Bug tracker](https://github.com/manticoresoftware/manticore/issues)

# How we can support you
Should your company require any help - we provide full-cycle services in the areas of Sphinx and Manticore Search:
  * Audit
  * Support
  * Consulting
  * Development
  * Training

[More details here](https://manticoresearch.com/services/)

# ❤️ How you can support Manticore Search

Manticore Search is a GPLv2-licensed open source project with development made possible by support from our core team, contributors, and sponsors. Building premium open-source software is not easy. If you would like to make sure Manticore Search stays free here is how:

* [Donation through PayPal](https://www.paypal.me/manticoresearch)
* [Become our client and let us help you](https://manticoresearch.com/services)

[![Analytics](https://ga-beacon.appspot.com/UA-114439919-1/manticoresoftware/manticore/README.md?pixel&useReferer)](https://github.com/manticoresoftware/manticore)
