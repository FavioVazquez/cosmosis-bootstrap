# cosmosis-bootstrap

This project contains scripts for the bootstrapping of CosmoSIS. Based on https://bitbucket.org/mpaterno/cosmosis-bootstrap.

You can use it to do an initial installation of CosmoSIS; it will download and install the most recent version of CosmosSIS, and the corresponding versions of all of its dependencies.
CosmoSIS itself resides in the repository at https://bitbucket.org/joezuntz/cosmosis/wiki/Home.

## USAGE: 

- cosmosis-bootstrap [options] <target-directory>

### OPTIONS:

    -?: Print this help and exit
    -d: Install Planck and WMAP data packages (large download)
    -e: Install external repositories, e.g. des (comma separated list)
    -h: Print this help and exit
    -k: Download in insecure mode, ignoring security certificates.  This is dangerous.
    -p: Skip installing python and related packages
    -r: Remove UPS installation tarballs after installation (this saves disk space)
    -t: After cloning the CosmoSIS repository, check out this tag (-x overrides this)
    -u: Use an existing CosmoSIS UPS installation (d option is ignored).
    -x: Check out the latest development version of cosmosis (bleeding edge; you can always update later)

'target-directory' is the directory under which everything is
installed. It will be created if necessary.

This installation is specific for Ubuntu systems (14.04 or 16.04). It is based on the official installation4
but with some tweaks. It was the code used for the development of this work, and the git branch for
the thesis will remain active for reproducibility.

Everything this script installs is put in a single directory which can be cleanly deleted and will not
interfere with your other installed programs.


## Prerequisites:

- Update and upgrade Ubuntu repositories and libraries:

```bash
sudo apt-get update 
sudo apt-get upgrade
```

- Install git:

```bash
sudo apt-get install git
```

- Install curl:

```bash
sudo apt-get install curl
```

## Instructions:

- Download and execute the bootstrap script by running the following lines. Make sure you are
running the bash shell.

```
curl -L --remote-name https://raw.githubusercontent.com/faviovazquez/cosmosis-bootstrap/master/cosmosis-bootstrap
chmod u+x cosmosis-bootstrapt
./cosmosis-bootstrap -d <new desired target directory e.g. "cosmosis">
```

The `-d` will download data from Planck and WMAP, so if you want a faster download omit it.
You can always download them later.

- Go to your new cosmosis directory with:

```
cd <the new desire target directory that just got created>
```

- Set up the CosmoSIS environment (this must be done every time you use the program):

```
source config/setup-cosmosis
```



- Build CosmoSIS libraries and included modules:

```
make
```
