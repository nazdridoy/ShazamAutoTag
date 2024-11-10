# ShazamAutoTag

This Python script automatically recognizes audio files (MP3 and OPUS) using Shazam, renames them according to the recognized song title and artist, and updates their tags and cover art.

## Installation

Before running the script, you need to install the required Python libraries. You can install them using the provided `requirements.txt` file.

```
pip install -r requirements.txt
```

## Usage

Ensure you have Python 3.6 or newer installed on your system.

Clone this repository or download the script and requirements.txt file.
Install the required libraries as mentioned above.
To use the script, you can run it in two ways:

```bash
./ShazamAutoTag [options]    # On Unix-like systems (Linux/MacOS)
# OR
python ShazamAutoTag [options]  # Works on all systems
```

Note: On Unix-like systems (Linux/MacOS), you might need to make the script executable first:
```bash
chmod +x ShazamAutoTag
```

## Options

- `-di`, `--directory` <directory>: Specify the directory where audio files are located for processing. If not specified, the script uses its current directory.

- `-te`, `--test`: Execute a test function to verify the script's functionality. It looks for files named "fileToTest.mp3" and "fileToTest.opus" in a `test` folder and checks the renaming process.

- `-m`, `--modify` <True/False>: Indicate whether the script should apply modifications to the audio tags and filenames. Defaults to `True`.

- `-de`, `--delay` <delay>: Specify a delay (in seconds) to wait before retrying the Shazam API call if the initial attempt fails. Defaults to 10 seconds.

- `-n`, `--nbrRetry` <number>: Specify the number of retries for the Shazam API call if it fails. Defaults to 10 tries.

- `-tr`, `--trace`: Enable tracing to print messages during the recognition and renaming process. Useful for debugging or monitoring script progress.

- `-h`, `--help`: Display help information showing all command-line options. 