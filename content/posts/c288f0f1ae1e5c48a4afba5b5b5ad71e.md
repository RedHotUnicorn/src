---
title: "GitHub - iterative/dvc: \U0001F989 ML Experiments and Data Management with
  Git"
date: 2023-06-22
src_link: https://www.notion.so/iterative-dvc-Data-Version-Control-Git-for-Data-Models-ML-Experiments-Management-7409921d5f9a44d3a55b5a940e3ab533
src_date: '2023-06-22 12:53:00'
gold_link: https://github.com/iterative/dvc
gold_link_hash: c288f0f1ae1e5c48a4afba5b5b5ad71e
tags:
- '#host_github_com'
---

[![](https://camo.githubusercontent.com/7b353ba916e041b4682c187851b808fff7143f40031eb7a6422ba84f3f1abee9/68747470733a2f2f6476632e6f72672f696d672f6c6f676f2d6769746875622d726561646d652e706e67)](https://dvc.org)


[![](https://github.com/iterative/dvc/workflows/Tests/badge.svg?branch=main)](https://github.com/iterative/dvc/actions) [![](https://camo.githubusercontent.com/c7a157e2cd807aaf862a4b7214c1d2bd8cebc149c263557da90b2d203ceff930/68747470733a2f2f696d672e736869656c64732e696f2f707970692f707976657273696f6e732f647663)](https://pypi.org/project/dvc) [![](https://camo.githubusercontent.com/8715da72e3848a285c223ac40368c8b2001f4d86734e7b1cc62f0a18c0f9df8c/68747470733a2f2f636f6465636f762e696f2f67682f6974657261746976652f6476632f6272616e63682f6d61696e2f67726170682f62616467652e737667)](https://codecov.io/gh/iterative/dvc) [![](https://camo.githubusercontent.com/0350534562328e569f6c577f31a818ca777d9cbdd38f3fb5c1c80d9e6f0fea7e/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f444f492d31302e353238312f7a656e6f646f2e333637373535332d626c75652e737667)](https://doi.org/10.5281/zenodo.3677553)


[![](https://camo.githubusercontent.com/bfb4e41fb4f3ee133a761a16296e6dae1da8f56681e0fd54a4069eee64add0c3/68747470733a2f2f696d672e736869656c64732e696f2f707970692f762f6476632e7376673f6c6162656c3d706970266c6f676f3d50795049266c6f676f436f6c6f723d7768697465)](https://pypi.org/project/dvc) [![](https://camo.githubusercontent.com/212368a2223dc001b9a2e025ea938d3d9ed5efe49efc6fb324752af003b608da/68747470733a2f2f696d672e736869656c64732e696f2f707970692f646d2f6476632e7376673f636f6c6f723d626c7565266c6162656c3d446f776e6c6f616473266c6f676f3d70797069266c6f676f436f6c6f723d676f6c64)](https://pypi.org/project/dvc) [![](https://camo.githubusercontent.com/18c9755e76b26ac16eaeac3cfcdc52a7ae73d895c78c22710987a2a894a4b5c6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f646562253743706b6725374372706d2537436578652d626c7565)](https://dvc.org/doc/install) [![](https://camo.githubusercontent.com/45a6a79188da997b91b90c51bf832089f052b99c995ff240a650ab7175e3eb8b/68747470733a2f2f696d672e736869656c64732e696f2f686f6d65627265772f762f6476633f6c6162656c3d62726577)](https://formulae.brew.sh/formula/dvc) [![](https://camo.githubusercontent.com/920e3217cc0ffb61ac9ac639cd9377eeca8a3d9c3697971585ba0fea1850a7b7/68747470733a2f2f696d672e736869656c64732e696f2f636f6e64612f762f636f6e64612d666f7267652f6476632e7376673f6c6162656c3d636f6e6461266c6f676f3d636f6e64612d666f726765)](https://anaconda.org/conda-forge/dvc) [![](https://camo.githubusercontent.com/b945daacb7f0c1e0c48903fa1a4a60af6e50da523f40b1775695a572a4b656ba/68747470733a2f2f696d672e736869656c64732e696f2f63686f636f6c617465792f762f6476633f6c6162656c3d63686f636f)](https://chocolatey.org/packages/dvc) [![](https://camo.githubusercontent.com/0a898e4a3d84a2ef16c587236f22d4b241f12532606f14dc06f27c1886e776d9/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f736e61702d696e7374616c6c2d3832424541302e7376673f6c6f676f3d736e61706372616674)](https://snapcraft.io/dvc)


**Data Version Control** or **DVC** is a command line tool and [VS Code Extension](#vs-code-extension) to help you develop reproducible machine learning projects:


1. **Version** your data and models. Store them in your cloud storage but keep their version info in your Git repo.
2. **Iterate** fast with lightweight pipelines. When you make changes, only run the steps impacted by those changes.
3. **Track** experiments in your local Git repo (no servers needed).
4. **Compare** any data, code, parameters, model, or performance plots.
5. **Share** experiments and automatically reproduce anyone's experiment.


Quick start
===========



> Please read our [Command Reference](https://dvc.org/doc/command-reference) for a complete list.


A common CLI workflow includes:




| Task | Terminal |
| --- | --- |
| Track data | `$ git add train.py params.yaml` `$ dvc add images/` |
| Connect code and data | `$ dvc stage add -n featurize -d images/ -o features/ python featurize.py` `$ dvc stage add -n train -d features/ -d train.py -o model.p -M metrics.json python train.py` |
| Make changes and experiment | `$ dvc exp run -n exp-baseline` `$ vi train.py` `$ dvc exp run -n exp-code-change` |
| Compare and select experiments | `$ dvc exp show` `$ dvc exp apply exp-baseline` |
| Share code | `$ git add .` `$ git commit -m 'The baseline model'` `$ git push` |
| Share data and ML models | `$ dvc remote add myremote -d s3://mybucket/image_cnn` `$ dvc push` |


How DVC works
=============



> We encourage you to read our [Get Started](https://dvc.org/doc/get-started) docs to better understand what DVC does and how it can fit your scenarios.


The closest *analogies* to describe the main DVC features are these:


1. **Git for data**: Store and share data artifacts (like Git-LFS but without a server) and models, connecting them with a Git repository. Data management meets GitOps!
2. **Makefiles** for ML: Describes how data or model artifacts are built from other data and code in a standard format. Now you can version your data pipelines with Git.
3. Local **experiment tracking**: Turn your machine into an ML experiment management platform, and collaborate with others using existing Git hosting (Github, Gitlab, etc.).


Git is employed as usual to store and version code (including DVC meta-files as placeholders for data). DVC [stores data and model files](https://dvc.org/doc/start/data-management) seamlessly in a cache outside of Git, while preserving almost the same user experience as if they were in the repo. To share and back up the *data cache*, DVC supports multiple remote storage platforms - any cloud (S3, Azure, Google Cloud, etc.) or on-premise network storage (via SSH, for example).


[![](https://camo.githubusercontent.com/ab63e023438880d76200b9eb966f8acf0a7e6bf59e23a162e38caceeb20ae324/68747470733a2f2f6476632e6f72672f696d672f666c6f772e676966)](https://dvc.org/img/flow.gif)


[DVC pipelines](https://dvc.org/doc/start/data-management/data-pipelines) (computational graphs) connect code and data together. They specify all steps required to produce a model: input dependencies including code, data, commands to run; and output information to be saved.


Last but not least, [DVC Experiment Versioning](https://dvc.org/doc/start/experiments) lets you prepare and run a large number of experiments. Their results can be filtered and compared based on hyperparameters and metrics, and visualized with multiple plots.


VS Code Extension
=================


To use DVC as a GUI right from your VS Code IDE, install the [DVC Extension](https://marketplace.visualstudio.com/items?itemName=Iterative.dvc) from the Marketplace. It currently features experiment tracking and data management, and more features (data pipeline support, etc.) are coming soon!


[![](https://raw.githubusercontent.com/iterative/vscode-dvc/main/extension/docs/overview.gif)](https://raw.githubusercontent.com/iterative/vscode-dvc/main/extension/docs/overview.gif)



> Note: You'll have to install core DVC on your system separately (as detailed below). The Extension will guide you if needed.


Installation
============


There are several ways to install DVC: in VS Code; using `snap`, `choco`, `brew`, `conda`, `pip`; or with an OS-specific package. Full instructions are [available here](https://dvc.org/doc/get-started/install).


Snapcraft (Linux)
-----------------


[![](https://camo.githubusercontent.com/0a898e4a3d84a2ef16c587236f22d4b241f12532606f14dc06f27c1886e776d9/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f736e61702d696e7374616c6c2d3832424541302e7376673f6c6f676f3d736e61706372616674)](https://snapcraft.io/dvc)



```
snap install dvc --classic
```

This corresponds to the latest tagged release. Add `--beta` for the latest tagged release candidate, or `--edge` for the latest `main` version.


Chocolatey (Windows)
--------------------


[![](https://camo.githubusercontent.com/b945daacb7f0c1e0c48903fa1a4a60af6e50da523f40b1775695a572a4b656ba/68747470733a2f2f696d672e736869656c64732e696f2f63686f636f6c617465792f762f6476633f6c6162656c3d63686f636f)](https://chocolatey.org/packages/dvc)



```
choco install dvc
```

Brew (mac OS)
-------------


[![](https://camo.githubusercontent.com/45a6a79188da997b91b90c51bf832089f052b99c995ff240a650ab7175e3eb8b/68747470733a2f2f696d672e736869656c64732e696f2f686f6d65627265772f762f6476633f6c6162656c3d62726577)](https://formulae.brew.sh/formula/dvc)



```
brew install dvc
```

Anaconda (Any platform)
-----------------------


[![](https://camo.githubusercontent.com/920e3217cc0ffb61ac9ac639cd9377eeca8a3d9c3697971585ba0fea1850a7b7/68747470733a2f2f696d672e736869656c64732e696f2f636f6e64612f762f636f6e64612d666f7267652f6476632e7376673f6c6162656c3d636f6e6461266c6f676f3d636f6e64612d666f726765)](https://anaconda.org/conda-forge/dvc)



```
conda install -c conda-forge mamba # installs much faster than conda
mamba install -c conda-forge dvc
```

Depending on the remote storage type you plan to use to keep and share your data, you might need to install optional dependencies: dvc-s3, dvc-azure, dvc-gdrive, dvc-gs, dvc-oss, dvc-ssh.


PyPI (Python)
-------------


[![](https://camo.githubusercontent.com/bfb4e41fb4f3ee133a761a16296e6dae1da8f56681e0fd54a4069eee64add0c3/68747470733a2f2f696d672e736869656c64732e696f2f707970692f762f6476632e7376673f6c6162656c3d706970266c6f676f3d50795049266c6f676f436f6c6f723d7768697465)](https://pypi.org/project/dvc)



```
pip install dvc
```

Depending on the remote storage type you plan to use to keep and share your data, you might need to specify one of the optional dependencies: `s3`, `gs`, `azure`, `oss`, `ssh`. Or `all` to include them all. The command should look like this: `pip install 'dvc[s3]'` (in this case AWS S3 dependencies such as `boto3` will be installed automatically).


To install the development version, run:



```
pip install git+git://github.com/iterative/dvc
```

Package (Platform-specific)
---------------------------


[![](https://camo.githubusercontent.com/18c9755e76b26ac16eaeac3cfcdc52a7ae73d895c78c22710987a2a894a4b5c6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f646562253743706b6725374372706d2537436578652d626c7565)](https://dvc.org/doc/install)


Self-contained packages for Linux, Windows, and Mac are available. The latest version of the packages can be found on the GitHub [releases page](https://github.com/iterative/dvc/releases).


### Ubuntu / Debian (deb)



```
sudo wget https://dvc.org/deb/dvc.list -O /etc/apt/sources.list.d/dvc.list
wget -qO - https://dvc.org/deb/iterative.asc | sudo apt-key add -
sudo apt update
sudo apt install dvc
```

### Fedora / CentOS (rpm)



```
sudo wget https://dvc.org/rpm/dvc.repo -O /etc/yum.repos.d/dvc.repo
sudo rpm --import https://dvc.org/rpm/iterative.asc
sudo yum update
sudo yum install dvc
```

Contributing
============


[![](https://camo.githubusercontent.com/c98b067f197032eaaf4502e78a2dfa4495a9886aad4d748be587ddd499004466/68747470733a2f2f636f6465636c696d6174652e636f6d2f6769746875622f6974657261746976652f6476632f6261646765732f6770612e737667)](https://codeclimate.com/github/iterative/dvc)


Contributions are welcome! Please see our [Contributing Guide](https://dvc.org/doc/user-guide/contributing/core) for more details. Thanks to all our contributors!


[![](https://camo.githubusercontent.com/9de9dc36f3d9c5dd22c9df6b257b87e00459028901d0406c7d2abc52d3c15b98/68747470733a2f2f636f6e747269622e726f636b732f696d6167653f7265706f3d6974657261746976652f647663)](https://github.com/iterative/dvc/graphs/contributors)


Copyright
=========


This project is distributed under the Apache license version 2.0 (see the LICENSE file in the project root).


By submitting a pull request to this project, you agree to license your contribution under the Apache license version 2.0 to this project.


Citation
========


[![](https://camo.githubusercontent.com/0350534562328e569f6c577f31a818ca777d9cbdd38f3fb5c1c80d9e6f0fea7e/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f444f492d31302e353238312f7a656e6f646f2e333637373535332d626c75652e737667)](https://doi.org/10.5281/zenodo.3677553)


Iterative, *DVC: Data Version Control - Git for Data & Models* (2020) [DOI:10.5281/zenodo.012345](https://doi.org/10.5281/zenodo.3677553).


Barrak, A., Eghan, E.E. and Adams, B. [On the Co-evolution of ML Pipelines and Source Code - Empirical Study of DVC Projects](https://mcis.cs.queensu.ca/publications/2021/saner.pdf) , in Proceedings of the 28th IEEE International Conference on Software Analysis, Evolution, and Reengineering, SANER 2021. Hawaii, USA.