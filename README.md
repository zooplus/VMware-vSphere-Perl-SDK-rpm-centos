-----------
Description
-----------

Build an RPM of `VMware-vSphere-Perl-SDK-*.x86_64.tar.gz` on CentOS6/CentOS7.


------------
Sample Usage
------------

Install VirtualBox and Vagrant https://www.virtualbox.org/ https://www.vagrantup.com/downloads.html

Build the RPM on the desired version of RHEL/CentOS:

        $ git clone https://github.com/zooplus/VMware-vSphere-Perl-SDK-rpm-centos.git
        $ cd VMware-vSphere-Perl-SDK-rpm-centos
        $ CENTOSVER=7.2 vagrant up

Perform a basic test of the RPM installed in the guest, `vmware-cmd` should exit without errors:

        $ vagrant ssh -c "source /opt/VMware-vSphere-Perl-SDK/bin/VMware-vSphere-Perl-SDK.sh&& vmware-cmd --help"

The RPMS are created under `./release/$CENTOSVER`.
CENTOSVER available from https://app.vagrantup.com/puppetlabs are supported (6.6, 7.2).

When done, destroy the VM with:

        $ vagrant destroy -f


------------
Dependencies
------------

None


-------
License
-------

BSD 2-clause


--------
Problems
--------
