[![tests](https://github.com/drud/ddev-addon-template/actions/workflows/tests.yml/badge.svg)](https://github.com/drud/ddev-addon-template/actions/workflows/tests.yml) ![project is maintained](https://img.shields.io/maintenance/yes/2023.svg)

# ddev-w3c-validator

## What is ddev-w3c-validator?

This repository provides the Nu Validator service for [DDEV](https://ddev.readthedocs.io).

It can be used to evaluate whether your HTML and CSS meets the W3C specifications.

## Use with Drupal

1. Enable the [W3C Validator](https://www.drupal.org/project/w3c_validator) module on your Drupal site.
2. Install this add-on: `ddev get ptmkenny/ddev-w3c-validator`
3. At `/admin/config/development/w3c_validator`, set the endpoint to `http://w3c-validator:8888`.
4. You can now run the scans from the Reports page: `/admin/reports/w3c_validator`.

## If you are on Apple Silicon/ARM

The scan will be really, really slow. For example, on a site of about 50 pages, it takes about 20 minutes to do the scan. This is because the Docker image does not support ARM.

If you want to speed this up, please give a [thumbs up to my feature request in the upstream repo](https://github.com/validator/validator/issues/1545).

**Contributed and maintained by [@ptmkenny](https://github.com/ptmkenny) based on the original [ddev-contrib recipe](https://github.com/ddev/ddev-contrib/tree/master/docker-compose-services/RECIPE) by [@ptmkenny](https://github.com/ptmkenny)**
