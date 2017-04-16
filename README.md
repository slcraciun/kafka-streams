# kafka-streams

[![Build Status](https://travis-ci.org/krystianity/kafka-streams.svg?branch=master)](https://travis-ci.org/krystianity/kafka-streams)

> (stateful) kafka stream processing 100% nodejs

[kafka-streams](http://docs.confluent.io/3.0.0/streams) :octopus: equivalent for nodejs :turtle: :rocket:  
build on super fast :fire: observables using [most.js](https://github.com/cujojs/most) :metal:  
ships with [sinek](https://github.com/krystianity/node-sinek) :pray: for backpressure  
overwriteable local-storage solution allows for any kind of datastore e.g. RocksDB, Redis, Postgres..  
async (Promises) and sync stream operators e.g. `stream$.map()` or `stream$.asyncMap()`  
super easy API :goberserk:   
the lib is based on `sinek`, which is based on kafka-node's `ConsumerGroups`
therefore it still requires a zookeeper connection (dont worry, your offset will be stored
in the kafka broker)

## Prerequisites
- kafka broker should be version `>= 0.9.x` 
- nodejs should be version `>= 6.10`

## Aim of this Library

- this is not a 1:1 port of the official JAVA kafka-streams
- the goal of this project is to give at least the same options to
a nodejs developer that kafka-streams provides for JVM developers
- stream-state processing, table representation, joins, aggregate etc.
I am aiming for the easiest api access possible checkout the [word count example](https://github.com/krystianity/kafka-streams/blob/master/examples/wordCount.js)

## Progress Overview (Port Adaption)

- [x] core structure
- [x] KStream - stream as a changelog
- [x] KTable - stream as a database
- [x] complex stream join structure
- [ ] windows (for joins)
- [x] word-count example
- [x] more examples
- [x] local-storage for etl actions
- [x] local-storage factory (one per action)
- [ ] KStorage example for any DB that supports atomic actions
- [ ] backing-up local-storage via kafka
- [x] kafka client implementation
- [x] KTable replay to Kafka (produce)
- [x] stream for topic message production only
- [x] sinek implementation
- [ ] backpressure mode for KafkaClient
- [ ] auto-json payloads (read-map/write-map)
- [ ] documentation
- [ ] API description
- [ ] higher join & combine examples
- [ ] ..

## Operator Implementations

- [x] map + asyncMap
- [ ] constant
- [ ] scan
- [ ] ap
- [ ] timestamp
- [x] tap
- [x] filter
- [x] skipRepeats
- [x] skipRepeatsWith
- [ ] slice
- [x] take
- [x] skip
- [ ] takeWhile
- [ ] skipWhile
- [ ] until
- [ ] since
- [ ] during
- [ ] thru
- [ ] reduce
- [x] forEach
- [ ] drain
- [x] _merge
- [ ] combine
- [ ] sample
- [ ] sampleWith
- [x] _zip
- [ ] switch
- [x] _join
- [ ] throttle
- [ ] debounce
- [ ] delay
- [x] multicast

## Additional Operators

- [x] mapStringToArray
- [x] mapArrayToKV
- [x] mapStringToKV
- [x] mapParse
- [x] mapStringify
- [x] atThroughput
- Want more? Feel free to open an issue :cop:

## Join Operations
- [x] merge
- [ ] outerJoin
- [ ] innerJoin
- [ ] leftJoin
- Want more? Feel free to open an issue :cop:

## Stream Action Implementations

- [x] countByKey
- [x] sumByKey
- [ ] ..
- Want more? Feel free to open an issue :cop:

## Can I use this library yet?

No, but very soon (aiming for end of April 2017).

## Are we ready for production yet?

No, please have some more patience :smile:

## More

Forks or Stars give motivation :bowtie:
