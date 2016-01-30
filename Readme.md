# Get YouTube Transcripts

## Purpose

Retrieve the plain text transcript from any YouTube video with a manually-created captions (auto-generated captions not currently supported.)

## Usage

### Positional arguments

`url` - The URL to the YouTube video you want to retrieve a transcript for.

### Optional arguments

`-h`, `—help` - show this help message and exit

`—file` - The path to the file you want to save transcript to. To use the video's title as the filename, specify a directory. Example: `~/Desktop/transcript.txt` or `~/Desktop`.

`—overwrite` - Overwrites existing file at save location, if present.

`—open` - Open the created transcript.

`—format` - Choose output format. Only used if `—file` argument is not specified.

- Valid options:
  - `dict`: Returns a Python dictionary.
  - `pipes`: Returns positional values separated by `|`. Order: *title*, *filename*, *transcript*.

### Example

``` shell
./get_transcript.py https://www.youtube.com/watch?v=<ID> --file ~/Desktop/
```

## Compatibility

* Python 2.7.11
* Should be platform-independent. Tested on OS X, Windows 10, & Linux.