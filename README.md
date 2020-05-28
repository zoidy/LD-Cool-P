# DataRepository_curation

- [Overview](#overview)
- [Getting Started](#getting-started)
    - [Requirements](#requirements)
    - [Installation Instructions](#installation-instructions)
    - [Testing Installation](#testing-installation)
- [Execution](#execution)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)

--------------

## Overview

This software tool is designed to enable the curatorial review of datasets
that are deposited into the [University of Arizona Research Data Repository (ReDATA)](https://arizona.figshare.com).
It follows a workflow that was developed by members of the
[Research Data Services Team](https://data.library.arizona.edu/) at the
[University of Arizona Libraries](https://new.library.arizona.edu/).
The software has a number of backend features, such as:
 1. Retrieving private datasets from the [Figshare API](https://docs.figshare.com)
    that are undergoing curatorial review
 2. Identifying whether a README.txt file is present in the ReDATA deposit.
    If such a file does not exists, it will provide ReDATA curators a
    copy of the [README.txt template](https://osf.io/sj8xv/download).
    Ultimately, it will perform an inspection to ensure that the README.txt
    adheres to a defined format and populates metadata information based on
    information submitted to ReDATA
 3. Retrieving a [Deposit Agreement Form](https://bit.ly/ReDATA_DepositAgreement)
    from Qualtrics, which is a requirement for all ReDATA deposits
 4. Retrieving a copy of [Curatorial Review Report template (MS-Word)](https://bit.ly/ReDATA_CurationTemplate)
    for ReDATA curators to complete.
 5. Supporting ReDATA curators with access and workflow management through
    standard UNIX commands

These backend services ingest the datasets and accompanying files (described above)
onto a curatorial "staging" server with attached storage to enable the full
curatorial review procedure.

Although not available yet, a web application will serve as the front-end
framework to allow for easy navigation through the curatorial review. Also,
integration with the [Trello REST API](https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
is another feature to further assist with the curatorial review process.


## Getting Started

These instructions will have the code running on your local or virtual machine.


### Requirements

You will need the following to have a working copy of this software. See
[installation](#installation-instructions) steps:
1. Python (3.7.5)
2. [`pandas`](https://pandas.pydata.org/) ([1.0.2](https://pandas.pydata.org/pandas-docs/version/1.0.2/))
3. [`requests`](https://requests.readthedocs.io/en/master/2.22.0)
4. [`numpy`](https://numpy.org/devdocs/release/1.17.4-notes.html/1.17.4)


### Installation Instructions

#### Python and setting up a `conda` environment

First, install a working version of Python (v3.7.5).  We recommend using the
[Anaconda](https://www.anaconda.com/distribution/) package installer.

After you have Anaconda installed, you will want to create a separate `conda` environment
and activate it:

```
$ (sudo) conda create -n curation python=3.7.5
$ conda activate curation
```

Next, clone this repository into a parent folder:

```
(curation) $ cd /path/to/parent/folder
(curation) $ git clone https://github.com/ualibraries/DataRepository_curation.git
```

With the activated `conda` environment, you can install with the `setup.py` script:

```
(curation) $ cd /path/to/parent/folder/DataRepository_curation
(curation) $ (sudo) python setup.py develop
```

This will automatically installed the required `pandas`, `requests`, and `numpy` packages.

You can confirm installation via `conda list`

```
(curation) $ conda list datarepository-curation
```

You should see that the version is `0.7.0`.


### Testing Installation

This section is under construction

## Execution

This section is under construction

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the
[tags on this repository](https://github.com/ualibraries/DataRepository_curation/tags).


## Authors

* Chun Ly, Ph.D. ([@astrochun](http://www.github.com/astrochun)) - [University of Arizona Libraries](https://github.com/ualibraries), [Office of Digital Innovation and Stewardship](https://github.com/UAL-ODIS)

See also the list of
[contributors](https://github.com/ualibraries/DataRepository_curation/contributors) who participated in this project.


## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT) - see the [LICENSE](LICENSE) file for details.
