<p align="center">
  <a href="https://mux.com/">
    <img src="https://avatars.githubusercontent.com/u/16199997?s=200&v=4" alt="Mux Logo">
  </a>
</p>

# Mux Data Monitoring Samples

Mux provides a mechanism for partners to subscribe to realtime video view level datastream of events and measurements related to the quality of service for integrated customers. Monitoring Samples are provided with 30 second granularity. This can be used to identify service-level problems, such as widespread rebuffering or playback failures.

The data is delivered in nested Protobuf format. A single stream samples “payload” may contain multiple samples from both time ranges and customer id’s.

Each sample corresponds to a single active video view. The sample can contain multiple records, where each record contains metrics for a point in time for the video view. A record specifies a time period and Metrics measured over that time period. All Metrics inside a single record will apply to the time range implied by the “start” timestamp field plus the “duration_ms” field. If the duration field is zero, the Record includes instantaneous Metrics. A Record MUST contain at least one Metric.

In addition to the information displayed in the monitoring dashboard, Monitoring Samples includes information about the CDN, allowing you to isolate poorly performing groups at the CDN level and steer those accordingly.
