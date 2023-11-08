
## Organization Github / Nextcloud

We would like have a simple way to share data and code. Therefore, we use the following structure:

The whole project is synced via NextCloud, with the exception of a folder named `github-repo` (this folder is manually removed from any synchronization with the NextCloud client). The content of this folder is this very repository. `tree .. -L 2` gives the following structure:



```
..
├── data-processed
│   ├── DHM
│   ├── Forest
│   ├── Mask
│   ├── Population
│   ├── Ticks
│   └── Weather
├── data-raw
│   ├── classified
│   ├── internal
│   └── public
├── data-temp
│   ├── DHM
│   ├── Population
│   ├── swissTLM
│   └── Weather
└── git_repo
    ├── 01_Clean_reports.qmd
    ├── 02_Prepare_covariates.qmd
    ├── _freeze
    ├── images
    ├── index.qmd
    ├── _quarto.yml
    └── Readme.md
```



## Data Portals in Switzerland

- <https://map.geo.admin.ch>: A beautiful, fast webgis to browse and explore swiss datasets. Most of the Geodatasets are visible here
- <https://www.swisstopo.admin.ch/>: the swiss federal office of topography. They provide most of the national available geodata. Interesting for us are following subsites:
  - [Landscape Models](https://www.swisstopo.admin.ch/en/geodata/landscape.html)
  - [Height Models](https://www.swisstopo.admin.ch/en/geodata/height.html)
- <https://geodienste.ch/>: For cantonal data. In the future, the dataset AV could be interesting for us.

## Swiss Coordinate Systems

- Switzerland has two local coordinate systems:


| Name            | EPSG  | Description                              | Axis names  | x-Range   | y-Range    |
|-----------------|-------|----------------------------------------- |-------------|----------:|-----------:|
| `CH1903 / LV03` | 21781 | Old coordinate system / Bessel ellipsoid | X/Y         |  600'000  |    200'000 |
| `CH1903+ / LV95`| 2056  | New coordinate system / Bessel ellipsoid | E/N         | 1'200'000 |  2'600'000 |


