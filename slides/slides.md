---
author: Filipe Fernandes
title: State of the IOOS Tools
date: May 1, 2018
---


# Longer title

The State of IOOS **(and some non-IOOS)** **(Python)** tools **(and its 105 repositories!?)**

# `whoami`

[ocefpaf]((https://github.com/ocefpaf))

>- Physical Oceanographer
>- Data Plumber
>- Code Janitor
>- CI babysitter
>- Amazon-Dash-Button for conda-forge

. . .

I'll probably have to add "GH Marie Kondo" after this presentation.

# Some background

>- year 01: skill score (SECOORA), system-test notebooks, packaging (ioos channel).
>- year 02: python 3 updates, CIs maintenance, packaging (conda-forge channel).
>- year 03: CIs maintenance, Data Demo Center, some new tools, packaging.
>- year 04: CIs maintenance, some Data Demo Center, less new tools, packaging.
>- year 05: CIs maintenance, Data Demo Center(?), new tools(?), packaging.



# Goals

>- Streamline CI maintenance (2-3 times a year we re-do the CIs configurations).
>- Reduce the overall maintenance burden.
>- Focus on the essential tools, deprecate what is not used.
>- What tools are ready for Python 2.7 EOL?

. . .

Spoiler: our tools are 100% py3k compatible!

# Goals (continued)

>- Identify gaps in our tools and/or if we need new ones to deal with new challenges (bio-obis-taxa?).
>- Increase the "bus" factor by making it easier for newcomers.
>- Create a policy for releases, *sdist* publication, and packaging.

. . .

Secret motivation: make year 06 all about new tools and the Data Demo Center!


# How?

>- Finding the active and inactive projects and deprecating the latter.
>- Consolidate similar tools.
>- Adding auto-PyPI *sdist* publication.
>- Adopt a Release Early Release Often (RERO) policy.
>- Write documentation of GH good practices.

# IOOS tools "health metric"

[https://bit.ly/2019-DMAC](https://bit.ly/2019-DMAC)

>- The data was collected on April 27th 2019.
>- The metric is based on: last commit, last release, number contributors, and py3k testing

# IOOS tools

| software           | last commit | last release | contributors | py3k testing |
|--------------------|-------------|--------------|--------------|--------------|
| compliance-checker | 2019-04-24  | 2019-02-27   | 28           | py37         |
| erddapy            | 2019-04-21  | 2019-03-06   | 3            | py37         |
| cc-plugin-glider   | 2019-02-20  | 2019-02-20   | 8            | py36         |
| cc-plugin-ugrid    | 2019-01-09  | 2019-01-09   | 5            | py36         |
| pyoos              | 2019-02-24  | 2017-03-30   | 11           | py35         |
| ciso               | 2019-02-07  | 2019-02-07   | 2            | py37         |
| cc-plugin-ncei     | 2019-01-16  | 2017-10-17   | 4            | py36         |
| sensorml2iso       | 2018-09-12  | 2018-08-22   | 6            | py36         |
| odvc               | 2019-04-27  | 2018-03-02   | 3            | py37         |
| thredds_crawler    | 2018-03-16  | 2018-03-16   | 5            | py36         |
| petulant-bear      | 2016-02-03  | 2016-02-03   | 6            | py35         |
| wicken             | 2016-02-03  | 2016-02-03   | 5            | py35         |
| qartod             | 2016-14-14  | NA           | 4            | py35         |
| cc-plugin-sgrid    | 2016-02-04  | NA           | 1            | py35         |

# Other Tools (pyoceans)

- `gridgeo`
- `ioos_tools`
- `pocean-core`
- ~~`erddapy`~~

. . .

There are more [tools in the pyoceans org](https://github.com/pyoceans).
I only listed those that I know are used by IOOS in some places.

# Other Tools (ASA-RPS)

WARNING: This list is not comprehensive!
Also, we are not expecting any action from ASA-RPS!
The goal is to identify what tools here are important to the IOOS community!

# Other Tools (ASA-RPS) list

- `qartod` (not a rare pókemon)
- `paegan`
- `paegan-viz`
- `paegan-transport`
- `sci-wms`
- `thredds_crawler_matlab`
- `udunitspy` (`compliace-checker` adopted `cf-units` instead)


# Other Tools (Axiom)

WARNING: This list is not comprehensive!
Also, we are not expecting any action from Axiom!
The goal is to identify what tools here are used and important to the IOOS community!

# Other Tools (Axiom) list

- `pyncml`
- `epic2cf`
- `wera2netcdf`
- `codar2netcdf`
- `modflow2netcdf`

# Other Tools (Axiom) continuation

- `pygc`
- `sci-wms` (déjà vu)
- `pyaxiom` (predecessor of `pocean-core`)
- `ioos_qc` (`qartod` pókemon evolved form)
- `pngpack`

# Other-Other Tools

- MetOffice stack: `iris`, `cartopy`, `nc-time-axis`, and `cf-units`
- PyViz: `bokeh`, `panel`, `hvplot`
- `bagit`
- `folium`
- `geopandas`
- `gsw`
- `matplotlib`
- `nco`

# Other-Other Tools (continuation)

- `netcdf4`
- `pysgrid`
- `pyugrid`
- `utide`
- `windrose`
- `xarray`
- `gridded`

. . .

Feel free to add more in the hackpad.

# Small aside: best practices

>- Always have a README file.
>- Always publish on PyPI.
>- Always add test with new code.
>- Auto-publish docs and `sdist` is a plus.
>- Adopting `black` and `isort` can be daunting at first but pays off in the end.
>- Should we have an IOOS boilerplate repo?

. . .

Some of these are part of the [PyOpenSci packaging guide](https://www.pyopensci.org/dev_guide/packaging/packaging_guide).

# Repositories

- catalog-docker-base
- catalog-docker-ckan
- catalog-docker-ckan-harvest
- catalog-docker-pycsw
- comt
- comt-landing
- comt_1_archive
- comt_2
- configuration-management
- configuration-management-hugo

# Repository clean-up Recommendations

>- Aggressive archiving of repositories to avoid user confusion.
>- Do not delete so we can revert the archived version if needed.
>- Add a README.{md,txt,rst} file to all active repositories!
>- Aggregate pages and docs into a sub-org/prefix.
>- Add Repo Health app: [https://repohealth.info](https://repohealth.info).

. . .

[https://repohealth.info/report/pyoceans/python-ctd](https://repohealth.info/report/pyoceans/python-ctd)


# Code gallery

<img src="images/code-gallery.png" height=450>

[http://ioos.github.io/notebooks_demos/code_gallery](http://ioos.github.io/notebooks_demos/code_gallery)

# PyViz demo


<a href="https://mybinder.org/v2/gh/ocefpaf/2019-DMAC/gh-pages?filepath=notebooks/GreatLakes_Dashboard.ipynb">
  <img src="images/jupyterhub.svg" height=75 style="background-color:white">
</a>


# end

![](images/twitter-github.png)

([ocefpaf]((https://github.com/ocefpaf)))


[https://ocefpaf.github.io/2019-DMAC](https://ocefpaf.github.io/2019-DMAC)
