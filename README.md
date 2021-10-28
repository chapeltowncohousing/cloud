
<!-- README.md is generated from README.Rmd. Please edit that file -->

# cloud

<!-- badges: start -->
<!-- badges: end -->

The goal of this repo is to document the cloudron service for Chaco.

Long term the plan is to host cloudron on premises but for the purposes
of testing a test server was set-up on Ubuntu 20.04 as follows, based on
instructions from
[Hetzner](https://community.hetzner.com/tutorials/howto-hcloud-cli):

``` bash
gh repo create chapeltowncohousing/cloud # create the repo with GitHub's CLI tool
sudo apt install hcloud # install hetzner cloud CLI tool
hcloud context create chaco # message: Context chaco created and activated
```

``` bash
hcloud context list
#> ACTIVE   NAME
#> *        chaco
```
