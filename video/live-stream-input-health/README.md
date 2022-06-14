<p align="center">
  <a href="https://mux.com/">
    <img src="https://avatars.githubusercontent.com/u/16199997?s=200&v=4" alt="Mux Logo">
  </a>
</p>

# Mux Video Live Stream Input Health Event Stream

Mux can now stream livestream health and metadata events for customers to an Amazon Kinesis endpoint in the customer’s cloud account. This feature is currently in closed beta for customers interested in testing the feature.

`LiveStreamInputHealth` events are sent to Kinesis as they are emitted and are made available to customers to retrieve from the stream within about one minute. Each `LiveStreamInputHealth` event will contain details for either a `RTMPMetadataEvent` or `HealthUpdateEvent`. Protobuf definitions for consuming the livestream input health events are in `proto/v1/livestreaminputhealth_v1.proto`.

This spec also supports Google Pub/Sub Schema requirements ([here](https://cloud.google.com/pubsub/docs/schemas#schema_types)) for future consumption with Pub/Sub.
