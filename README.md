# R container and ext libraries 
- first build the container following [instructions](https://github.com/GITC2025/R_container_5sep2026/blob/main/R4.5.3_container.md)
- this container is locked down (no internet access), preventing version drift
- to add libraries, either add them to external libraries, or remake the container
- when downloading new libraries - check for all required dependencies 

## Rocker 4.5.3
- this container is built on Rocker 4.5.3
- if you want a bare minimum container, use the official [Rocker 4.5.3](https://hub.docker.com/r/rocker/r-ver/tags)

## ext libraries - 5 sep version 
```sh
# download the pre-compiled library archive
curl -fsSL -O https://github.com/GITC2025/R_container_5sep2026/releases/download/v1.0.0/R_ext_libraries_24July2026.tar.gz

# extract into your destination directory
tar -xvzf R_ext_libraries_24July2026.tar.gz
```

## to use in R
```
# add the extracted library path to your search path
.libPaths(c("/path/to/R_ext_libraries_24July2026", .libPaths()))
```
