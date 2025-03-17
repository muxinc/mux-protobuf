<p align="center">
  <a href="https://mux.com/">
    <img src="https://avatars.githubusercontent.com/u/16199997?s=200&v=4" alt="Mux Logo">
  </a>
</p>

# Mux Data Streaming Exports of Video Views

Mux Data can stream views for customers on Media plan to an Amazon Kinesis or Google Pub/Sub endpoint in the customer’s cloud account. Views are sent to Kinesis or Pub/Sub as they complete and are made available to customers to retrieve from the stream within about one minute after the view ends.

See our [Streaming Exports guide](https://docs.mux.com/guides/data/export-raw-video-view-data#stream-views-as-they-complete) for more information on setting up streaming exports of video views.

## Streaming Exports Versioning

As Mux Data adds new metrics, new versions of the protobuf specification are released. This repository always contains the most up-to-date specification. See our guide on [understanding the data fields](https://docs.mux.com/guides/data/export-raw-video-view-data#understand-the-data-fields) to see a full list of supported metrics.

### Version 13

Added new standard dimensions:

- `used_captions`
- `used_pip`
- `video_affiliate`
- `audio_codec`
- `video_brand`
- `video_codec`
- `video_dynamic_range_type`
- `view_cdn_edge_pop`
- `view_cdn_origin`
- `client_application_name`
- `client_application_version`
- `view_drm_level`
- `time_shift_enabled`
- `viewer_plan`
- `viewer_plan_category`
- `viewer_plan_status`
- `video_creator_id`

### Version 12

Added more custom dimensions:

- `custom_11`
- `custom_12`
- `custom_13`
- `custom_14`
- `custom_15`
- `custom_16`
- `custom_17`
- `custom_18`
- `custom_19`
- `custom_20`

### Version 11

Added new dimension:

- `view_dropped`

### Version 10

Added new dimension:

- `ad_playback_failure_error_type_id`

Added new metrics:

- `view_content_startup_time`
- `ad_preroll_startup_time`
- `ad_playing_time`
- `view_content_playing_time`

### Version 9

Added new dimensions:

- `playback_failure_error_type_id`
- `playback_business_exception_error_type_id`
- `video_startup_business_exception_error_type_id`

Added new event metadata for error events (`player_error_severity` and `player_error_is_business_exception`)

### Version 8

Added new metrics:

- `ad_attempt_count`
- `ad_break_count`
- `ad_break_error_count`
- `ad_break_error_percentage`
- `ad_error_count`
- `ad_error_percentage`
- `ad_impression_count`
- `ad_startup_error_count`
- `ad_startup_error_percentage`
- `ad_exit_before_start_count`
- `ad_exit_before_start_percentage`

### Version 7

Added new dimension:

- `video_startup_failure`

### Version 6

Added new dimension:

- `view_has_ad`

### Version 5

Added new event metadata for `request_canceled`, `request_failed`, and `request_completed` events.

### Version 4

Added new event metadata for `ad` (`adplay`, `adplaying`, etc) and `error` events.

### Version 3

Added new dimensions:

- `custom_6`
- `custom_7`
- `custom_8`
- `custom_9`
- `custom_10`
- `view_drm_type`

Added new metric:

- `view_dropped_frame_count`

### Version 2

Added new dimension:

- `mux_embed`

### Version 1

Video View proto spec.
