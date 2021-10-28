
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

``` bash
hcloud server-type list
#> ID   NAME        CORES   MEMORY     DISK     STORAGE TYPE
#> 1    cx11        1       2.0 GB     20 GB    local
#> 2    cx11-ceph   1       2.0 GB     20 GB    network
#> 3    cx21        2       4.0 GB     40 GB    local
#> 4    cx21-ceph   2       4.0 GB     40 GB    network
#> 5    cx31        2       8.0 GB     80 GB    local
#> 6    cx31-ceph   2       8.0 GB     80 GB    network
#> 7    cx41        4       16.0 GB    160 GB   local
#> 8    cx41-ceph   4       16.0 GB    160 GB   network
#> 9    cx51        8       32.0 GB    240 GB   local
#> 10   cx51-ceph   8       32.0 GB    240 GB   network
#> 11   ccx11       2       8.0 GB     80 GB    local
#> 12   ccx21       4       16.0 GB    160 GB   local
#> 13   ccx31       8       32.0 GB    240 GB   local
#> 14   ccx41       16      64.0 GB    360 GB   local
#> 15   ccx51       32      128.0 GB   600 GB   local
#> 22   cpx11       2       2.0 GB     40 GB    local
#> 23   cpx21       3       4.0 GB     80 GB    local
#> 24   cpx31       4       8.0 GB     160 GB   local
#> 25   cpx41       8       16.0 GB    240 GB   local
#> 26   cpx51       16      32.0 GB    360 GB   local
#> 33   ccx12       2       8.0 GB     80 GB    local
#> 34   ccx22       4       16.0 GB    160 GB   local
#> 35   ccx32       8       32.0 GB    240 GB   local
#> 36   ccx42       16      64.0 GB    360 GB   local
#> 37   ccx52       32      128.0 GB   600 GB   local
#> 38   ccx62       48      192.0 GB   960 GB   local
```

Launch the server as follows:

``` bash
hcloud server create --image ubuntu-20.04 --type cx41 --name chaco
```
