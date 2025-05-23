**Building and running the swtpm has dependencies on the following packages**:

- automake
- autoconf
- bash
- coreutils
- expect
- libtool
- sed
- libtpms
- libtpms-devel
- fuse
- fuse-devel
- glib2
- glib2-devel
- json-glib-devel
- net-tools
- python3
- python3-twisted
- selinux-policy-devel
- socat
- trousers
- gnutls
- gnutls-devel
- libtasn1
- libtasn1-tools
- libtasn1-devel
- rpm-build (to build RPMs)

Debian/Ubuntu also needs the following packages to build:

- build-essential
- devscripts
- equivs

On RHEL or Fedora use either one of the following methods to install
the above dependencies:

 - sudo dnf builddep ./swtpm.spec  (Fedora >= 22)
 - sudo yum install yum-utils ; sudo yum-builddep ./swtpm.spec  (RHEL and Fedora <= 21)
 - sudo yum install <package name(s)>

On Ubuntu use the following command:

 - sudo mk-build-deps --install ./debian/control


Use the following sequence to build and install the Software TPM.

./autogen.sh --prefix=/usr
make
make check
make install


To build an rpm on a Fedora or RHEL host do:

./autogen.sh
make dist
rpmbuild -ta swtpm-*.tar.gz


To build a Debian package on a Debian compatible host do:

echo "libtpms0 libtpms" > ./debian/shlibs.local
debuild -us -uc
