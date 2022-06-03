# 0. Download Data

### Download Methods:

- ~~Donwload via [idr-py](https://github.com/IDR/idr-py)~~
  - [IDR_downloader.ipynb](../0.download_data/IDR_downloader.ipynb)
  - Files in .webp format, very compressed and easy to work with
  - No high-performance transfer client, ~27 days to download
  - [`ResourceError`](https://github.com/IDR/idr-py/issues/26) during download of 7th plate
- Donwload via [Aspera](https://idr.openmicroscopy.org/about/download.html)
  - Files in .cd5 ([CellH5](https://github.com/CellH5/cellh5)) format, large and difficult to work with
  - High-performance transfer client, ~6 days to download
  - [`OSError`](https://github.com/CellProfiler/python-bioformats/issues/159) when trying to load with python-bioformats
- Download via [idr bucket](https://www.openmicroscopy.org/2020/11/04/zarr-data.html)
  - Files in [OME-zarr](https://github.com/ome/ome-zarr-py) format, easy to work with
  - Unsure of high-performance transfer client ([ongoing issue](https://github.com/IDR/idr.openmicroscopy.org/issues/160))
