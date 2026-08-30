# Design News Feed 

## Problem Statement

## Requirements
### Functional Requirements

* Users can post/publish multi-media feeds and follow friends updates
* DAU=10M - System capacity, storage, TPS
* 5k friends/user - Fan-out design

### Non-Functional Requirements
> low latency: fetching the news feed fast is crucial
* pre-compute news feed with push model (Fan-out on write) for regular users
* news feed cache containing only <post_id, user_id> to reduce memory foot print
* media on CDN
* localized data center

> High availability and scalability: 
* redundant data center
* master-slave replication
* read-replica
* database sharding

> Reliability and System Overload prevention (Celebrity Hot Key problem)
* hybrid fand-out model: Celebrity VS regular users
* Celebrity: Pulled on-Demand by followers to prevent system overload
* Regular Users: (push) pre-computed
* consistent hashing: distribute requests and data evenly across cache nodes

> Security and Abuse prevention: 
* enforce strict authentication (security token)
* rate-limiting

> Configurable consistency (eventual consistency):
* not really that time sensitive on real time update -> eventual consistency is sufficient

## High Level Design
> Feed Publishing: how data flows for a user's post
> Newsfeed building: how data is displayed on user's UI


## Technical components
* CDN (when delivering media)
* How to deal with Fanout
* consistent hashing

## Notes
* mobile and web client: any design differences on those two platform?
* what is hotkey problem


