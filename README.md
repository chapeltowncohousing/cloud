
<!-- README.md is generated from README.Rmd. Please edit that file -->

# cloud

<!-- badges: start -->
<!-- badges: end -->

The goal of this repo is to document the cloudron service for Chaco.

Get the link for free credits at <https://www.cloudron.io/get.html>

Sign up to upcloud for free credits.

Select suitable location from upcloud:

![](images/paste-1.png)

Find your open ssh key as follows:

``` bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
cat ~/.ssh/id_rsa.pub
```

Then log in as follows:

``` bash
ssh root@xx.xxx.xx.xx
```

Install cloudron as follows:

``` bash
wget https://cloudron.io/cloudron-setup
chmod +x ./cloudron-setup
./cloudron-setup 
```

Set-up admin credentials as follows:

![](images/paste-2.png)

Follow the instructions on
<https://docs.cloudron.io/domains/#dns-providers> (manual mode is fine).

Install some apps!

![](images/paste-3.png)

(You need a cloudron.io account.)

&#10;
<!-- Long term the plan is to host cloudron on premises but for the purposes of testing a test server was set-up on Ubuntu 20.04 as follows, based on instructions from [Hetzner](https://community.hetzner.com/tutorials/howto-hcloud-cli): 
&#10;::: {.cell}
&#10;```{.bash .cell-code}
gh repo create chapeltowncohousing/cloud # create the repo with GitHub's CLI tool
sudo apt install hcloud # install hetzner cloud CLI tool
hcloud context create chaco # message: Context chaco created and activated
```
&#10;:::
&#10;::: {.cell}
&#10;```{.bash .cell-code}
hcloud context list
```
:::
&#10;::: {.cell}
&#10;```{.bash .cell-code}
hcloud server-type list
```
:::
&#10;
Launch the server as follows:
&#10;
::: {.cell}
&#10;```{.bash .cell-code}
hcloud server create --image ubuntu-20.04 --type cx41 --name chaco
```
:::
&#10;
-->
