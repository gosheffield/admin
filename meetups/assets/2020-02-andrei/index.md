# gRPC

## why

efficient
Not dealing with the messy input/response serialization baloney as gRPC deals with the serialization ― more efficient data encoding and HTTP/2 which makes things go faster with multiplexed requests over a single connection and header compression

structured
(Almost) No "design dichotomy" ― what's the right end-point to use, what's the right HTTP verb to use, etc.
Formalized set of errors ― this is debatable but so far they are more directly applicable to API use cases than the HTTP status codes

compatibility
Define/Declare your input/response and generate reliable clients for different languages (of course, the ones that are "supported", this is a HUGE advantage)

tooling
health checks
extensible

backwards compatibility

streaming

HTTP/2
full duplex streaming
binary framing
compression
conn multiplexing
largely follows HTTP, except for static paths for performance reasons during call dispatch

## why not

high adoption cost

opaque without proper tooling
how do I cURL this?

async
development overhead, complexity
serialization overhead
still small cost, on the order of 100s of µs
flatbuffers, capnproto cut that cost to zero (theoretically)

## alternatives

fat
rest (msgpack) -> devolves into restish
graphql
websocket

rpc
Apache Thrift
Apache Avro

messaging
zeromq
rabbitmq
kafka
nsq
nats

## protobuf

intro

## bells and whistles

well-known types
