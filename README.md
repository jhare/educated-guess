# educated-guess
Only trawl through the sites I give a fuck about and steal all other results. Also use other EG servers to tack on results

A lot of this is redundant between sections. But 'whaddyagonnado

### ODD - Outline Driven Design (it's not very good)
* plugin architecture
  * agent can take on one of many core roles of the architecture
  * data exchanged through HTTP JSON
  * May have to consider other engines to keep data flow small and efficient
* data model
* crawling
  * seed sites based on some cheating
* indexing
* scoring
* query
  * robust boolean query language
* federation
  * security features
  * share search results
  * share scoring
  * distribute what is possible
  * two servers can guess how similar they are to each other
* deferred optimization
* caching of results
* stealing results
* trusted vs. untrsuted results
* metrics
* event management

### Principles
* Use HTTP/JSON/CSV (simple shit) where we can to increase interconnectedness
* Directed search. A "general" search engine already exists
* Emphasize plugin architecture, loose coupling
  * Hey isn't messaging slow for the optimization needed for a search engine?
  * Oh for sure. I don't care though. We're searching smaller, but smarter.
* Limiting the domain reduces other constraints in search
* Allow a lot of cheating and human intervention. You'll never be the main engine.
* You can break shit with this server

### Search Constraints and Types
* General search
* "Discovery" search
* "Referential" search

### Data Model
* If a client/server can be in any language, the data model is the unifying element
* not necessarily all pieces are a client/server
  * crawler may submit results to indexer etc to delegate down the chain
  * Rely on RabbitMQ or AMQP more to kick off events

### Research
I realized I don't even know much past the basics that I *guessed*

* https://www.quora.com/How-do-you-build-a-search-engine-from-scratch-What’s-the-best-technology-stack-for-this
* https://blog.saush.com/2009/03/17/write-an-internet-search-engine-with-200-lines-of-ruby-code/
* https://softwareengineering.stackexchange.com/questions/47360/if-i-wanted-to-build-a-search-engine-how-would-i-start
* https://moz.com/blog/search-engine-algorithm-basics

### Related Neat Projects
* elastic (with Logstash https://elastic.co)
* apache solr
