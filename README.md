# Terrain
A shared repository for CAD/CAE graph transformations

## 19: Downloading terrain data
Download all hgt files for Poland (this will take a while, but can be safely interrupted).

```$ wget -r -nc -nH --accept-regex='.*N[1-5][0-9]E0[2-5][0-9].*' https://dds.cr.usgs.gov/srtm/version2_1/SRTM3/Eurasia/```

Compile `https://github.com/Podsiadlo/terrain` using

```cmake . && make```

Run 

```tergen -o out -Y -d Data/SRTM3 -x 3000 -y 3000 -z 3000 -i 1 -j 1 -k 1 -N 54.5 -S 49 -E 14.07 -W 24.09```

to get terrain data for poland
