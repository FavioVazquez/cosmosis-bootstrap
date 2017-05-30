# cosmosis-bootstrap

This project contains scripts for the bootstrapping of CosmoSIS. Based on https://bitbucket.org/mpaterno/cosmosis-bootstrap.

This project contains scripts for the bootstrapping of CosmoSIS. You can use it to do an initial installation of CosmoSIS; it will download and install the most recent version of CosmosSIS, and the corresponding versions of all of its dependencies.
CosmoSIS itself resides in the repository at https://bitbucket.org/joezuntz/cosmosis/wiki/Home.


### USAGE: 

- cosmosis-bootstrap [options] <target-directory>
- cosmosis-bootstrap installs the software upon which CosmoSIS depends.

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

