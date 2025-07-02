Script to flatten a dataset directory, rename files, convert frame rates, truncate frame counts, and convert JSON to TXT for diffusion pipeline.
- Reads from input_dir and writes to output_dir to avoid I/O issues
- Renames all files (json and media) to subfolder_original-filename
- Moves all files out of subfolders to the root of output_dir
- Converts video frame rates to specified framerate (if framerate > 0), showing start and final frame counts
- Truncates videos to specified framecap (if framecap > 0 and frame count exceeds cap)
- Matches the bitrate of the original video during processing
- Renames JSON files to .txt and retains only the 'long caption' values

Configure settings below.
Make sure you have ffmpeg and ffmpeg-python installed.

Example run command on Linux/Runpod:
```
apt-get update
apt-get install -y ffmpeg
pip install ffmpeg-python
pip install decord
pip install omegaconf
python convertFPS.py
```
