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

Please see geoips/CHANGELOG_TEMPLATE.rst for instructions on updating
CHANGELOG appropriately with each PR

Release notes for previous/upcoming versions can be found in docs/source/releases,
for reference.

Enhancements
============

Split product templates into family-based and product-defaults-based
--------------------------------------------------------------------

* This creates a second family-based product template to show both options for
  specifying a product.
* Reworked comments in plugins.

::

    added: my_package/plugins/yaml/products/amsr2_family.yaml
    deleted: my_package/yaml_configs/product_inputs/amsr2.yaml
    deleted: my_package/yaml_configs/product_params/89-Test.yaml
    renamed: my_package/plugins/yaml/product_defaults/89-Test.yaml my_package/plugins/yaml/product_defaults/89_PCT_Test.yaml
    renamed: my_package/plugins/yaml/products/amsr2_test.yaml my_package/plugins/yaml/products/amsr2_product_defaults.yaml
    renamed: tests/scripts/amsr2.global_clean.89-Test.sh tests/scripts/amsr2.global_clean.89-PCT-Product-Defaults.sh
    renamed: tests/scripts/amsr2.tc_clean.89-Test.sh tests/scripts/amsr2.tc_clean.89-PCT-Family.sh
