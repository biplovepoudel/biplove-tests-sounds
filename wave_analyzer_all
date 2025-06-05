import wave
import contextlib
import os

filename = 'example.wav'  # Replace with your file

# Check if file exists
if not os.path.exists(filename):
    print(f"File '{filename}' not found.")
else:
    with contextlib.closing(wave.open(filename, 'r')) as f:
        # Basic properties
        frames = f.getnframes()
        rate = f.getframerate()
        duration = frames / float(rate)
        channels = f.getnchannels()
        sampwidth = f.getsampwidth()  # in bytes per sample
        comptype = f.getcomptype()
        compname = f.getcompname()

        # File size in MB
        filesize_mb = os.path.getsize(filename) / (1024 * 1024)

        # Print metadata
        print("Audio File Metadata:")
        print(f"  File Name        : {filename}")
        print(f"  File Size        : {filesize_mb:.2f} MB")
        print(f"  Duration         : {duration:.2f} seconds")
        print(f"  Sample Rate      : {rate} Hz")
        print(f"  Channels         : {channels}")
        print(f"  Sample Width     : {sampwidth * 8} bits")
        print(f"  Compression Type : {comptype} ({compname})")
