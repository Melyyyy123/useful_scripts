                                               CHEATSHEET
                                             QUICK START
       Tip: It is recommended to create a new environment for any new project or workflow.

verify conda install and check version       conda info

update conda in base environment             conda update -n base conda
install latest anaconda distribution
                                             conda install anaconda=2022.05
(see release notes)
create a new environment
                                             conda create --name ENVNAME
(tip: name environment descriptively)
activate environment
                                             conda activate ENVNAME
(do this before installing packages)


                                  CHANNELS AND PACKAGES
 Tip: Package dependencies and platform specifics are automatically resolved when using conda.

list installed packages                      conda list

list installed packages with source info     conda list --show-channel-urls

update all packages                          conda update --all

install a package from specific channel      conda install -c CHANNELNAME PKG1 PKG2

install specific version of package          conda install PKGNAME=3.1.4

install a package from specific channel      conda install CHANNELNAME::PKGNAME

install package with AND logic               conda install “PKGNAME>2.5,<3.2”

install package with OR logic                conda install “PKGNAME [version=’2.5|3.2’]”

uninstall package                            conda uninstall PKGNAME

view channel sources                         conda config --show-sources

add channel                                  conda config --add channels CHANNELNAME
set default channel for pkg fetching
                                             conda config --set channel_priority strict
(targets first channel in channel sources)


                          WORKING WITH CONDA ENVIRONMENTS
Tip: List environments at the beginning of your session. Environments with an asterisk are active.

list all environments and locations          conda env list

list all packages + source channels          conda list -n ENVNAME --show-channel-urls

install packages in environment              conda install -n ENVNAME PKG1 PKG2

remove package from environment              conda uninstall PKGNAME -n ENVNAME

update all packages in environment           conda update --all -n ENVNAME
                                                 CHEATSHEET
                                    ENVIRONMENT MANAGEMENT
         Tip: Specifying the environment name confines conda commands to that environment.

 create environment with Python version       conda create -n ENVNAME python=3.10

 clone environment                            conda create --clone ENVNAME -n NEWENV

 rename environment                           conda rename -n ENVNAME NEWENVNAME

 delete environment by name                   conda remove -n ENVNAME --all

 list revisions made to environment           conda list -n ENVNAME --revisions

 restore environment to a revision            conda install -n ENVNAME --revision NUMBER

 uninstall package from specific channel      conda remove -n ENVNAME -c CHANNELNAME PKGNAME


                                    EXPORTING ENVIRONMENTS
     Recommendation: Name the export file “environment.” Environment name will be preserved.

 cross-platform compatible                    conda env export --from-history>ENV.yml

 platform + package specific                  conda env export ENVNAME>ENV.yml

 platform + package + channel specific        conda list --explicit>ENV.txt


                                    IMPORTING ENVIRONMENTS
         Tip: When importing an environment, conda resolves platform and package specifics.

 from a .yml file                             conda env create -n ENVNAME --file ENV.yml

 from a .txt file                             conda create -n ENVNAME --file ENV.txt


                                           ADDITIONAL HINTS
 get help for any command                     conda COMMAND --help

 get info for any package                     conda search PKGNAME --info
 run commands w/o user prompt                 conda COMMAND ARG --yes
 eg, installing multiple packages             conda install PKG1 PKG2 --yes
 remove all unused files                      conda clean --all

 examine conda configuration                  conda config --show



MORE RESOURCES                                                                FOLLOW US ON TWITTER!
Full Conda Documentation             conda.io                                           @anacondainc
Learning Resources                   anaconda.cloud                                     @condaproject



                                                                         conda cheat sheet Version 4.14.0
