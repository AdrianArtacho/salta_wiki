
# Data input

Data preparation and possible scenarios...

## transcoding / normalizing sampling rates

- Find out the framerate (for reference) using the terminal
- If the video needs to be converted from the device’s native format

Videos may require transcoding or cropping before analysis.
For example, the lines below ensure the correct frame rate is known prior to processing:

```bash
ffprobe -v error -select_streams v:0 \
-show_entries stream=r_frame_rate \
-of default=noprint_wrappers=1:nokey=1 your-video.mp4
```

Simple editing tasks (e.g., trimming) can be performed with VLC or iMovie,
avoiding re-encoding artefacts.

...

## synchronizing multiple data streams

...

## Cropping / masking

- If the video needs to be cropped before processing
