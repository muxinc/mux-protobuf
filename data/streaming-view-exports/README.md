<p align="center">
  <a href="https://mux.com/">
    <img src="https://avatars.githubusercontent.com/u/16199997?s=200&v=4" alt="Mux Logo">
  </a>
</p>

# Mux Data Streaming View Exports

Mux Data can stream views for customers on Media plan to an Amazon Kinesis or Google Pub/Sub endpoint in the customer’s cloud account. Views are sent to Kinesis or Pub/Sub as they complete and are made available to customers to retrieve from the stream within about one minute after the view ends. Protobuf definitions for consuming Mux Data streaming view exports are in `proto/exportstream.proto`.

See the [Mux Data Guide](https://docs.mux.com/guides/data/export-raw-video-view-data#stream-views-as-they-complete-beta) for more information on setting up streaming video exports


### Version 1

[Proto v1](proto/exportstream.proto)

Our original Streaming View Exports proto spec.  Wire-compatible with version 2, this version will be deprecated.
### Version 2 - latest 

[Proto v2](proto/exportstream/v2/exportstream_v2.proto)

Wire-compatible with version 1, we updated the spec to support Google Pubsub Schema requirements ([here](https://cloud.google.com/pubsub/docs/schemas#schema_types)).  This version has nested types and no external dependencies.

Due to the impact of nesting types instead of top-level types and defining `Timestamp` and `Duration` instead of importing, this change will break code generated from the `v1` implementation.
