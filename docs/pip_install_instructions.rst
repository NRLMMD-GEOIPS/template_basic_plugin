 | # # # Distribution Statement A. Approved for public release. Distribution unlimited.
 | # # #
 | # # # Author:
 | # # # Naval Research Laboratory, Marine Meteorology Division
 | # # #
 | # # # This program is free software: you can redistribute it and/or modify it under
 | # # # the terms of the NRLMMD License included with this program. This program is
 | # # # distributed WITHOUT ANY WARRANTY; without even the implied warranty of
 | # # # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the included license
 | # # # for more details. If you did not receive the license, for more information see:
 | # # # https://github.com/U-S-NRL-Marine-Meteorology-Division/


#############################################################
Instructions for using pip to install geoips packages and repositories
#############################################################

*IMPORTANT NOTE: In all commands below, replace @repository@ with the name of the geoips
repository that you want to install. Also, note the exported environment variables
needed to install to the correct locations.*

#. Export environment variables if not already completed
    # GeoIPS Default Locations
    * export GEOIPS_REPO_URL=https://github.com/NRLMMD-GeoIPS  # Point to base URL for git clone commands
    * export GEOIPS_PACKAGES_DIR=$HOME/geoips/geoips_packages
    * export GEOIPS_TESTDATA_DIR=$HOME/geoips/test_data
    * export GEOIPS_DEPENDENCIES_DIR=$HOME/geoips/geoips_dependencies

    # GeoIPS default configuration - must be source ANY TIME you want to run GeoIPS
    # You can create your own user/site specific version to replace this one as needed.

    * export GEOIPS_CONFIG_FILE=$GEOIPS_PACKAGES_DIR/geoips/setup/config_geoips

#. Change directories (cd) to your selected/cloned geoips @repository@

    * ``cd $GEOIPS_PACKAGES_DIR/@repository@``

#. Install @repository@ dependencies and associate them with the repository's environment

    * ``pip install -e $GEOIPS_PACKAGES_DIR/@repository@``
    * For doc, test, lint, archer, pytest, etc... installs, cd to cloned @repository@, using the command below. 
        You can omit packages included in the command if you don't want to install them.
        * ``pip install -e .[doc,test,lint,pytest,archer]``

#. List of useful pip install commands if needed - not specific to @repository@
    * ``pip install -use-pep517 pykdtree``
    * ``any other commands Mindy or Jeremy may know to be useful``

