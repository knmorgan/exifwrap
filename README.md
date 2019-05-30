# exifwrap

It seems that many devices which output videos do not include the necessary
metadata for the file to be properly sorted in an image viewer (e.g. Google
Photos). This tool is a helpful wrapper around exiftool, and can be used to set
the appropriate metadata field for easy sorting. The following command can be
used to manually set the date and time on a video.

```
exifwrap -t "2019:05:29 23:38:17-04:00" video.mp4
```

If one does not specify a timestamp it defaults to the file's last modify date.

```
exifwrap video.mp4
```

A flag can be set to bypass user input, which can be useful for batching.

```
exifwrap -f -t "2019:05:29 23:38:17-04:00" video.mp4
```
