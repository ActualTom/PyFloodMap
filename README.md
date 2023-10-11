# PyFloodMap
Python Flood Map for emergency managers - inspired by Kyle Pastor
Requires 4 subdirectories: depth, composite_images, satellite_images, elevation_images
Requires python3, mercantile, numpy, and ffmpeg

python3 floodmap.py

ffmpeg  -i ./depth/%04d.png -c:v libx264 -c:a aac -ar 44100 -filter "minterpolate='fps=30'" -pix_fmt yuv420p output.mp4
