-----------
Description
-----------

Build an RPM of `VMware-vSphere-Perl-SDK-*.x86_64.tar.gz` on CentOS6/CentOS7.


------------
Sample Usage
------------

Install VirtualBox and Vagrant https://www.virtualbox.org/ https://www.vagrantup.com/downloads.html

Download `VMware-vSphere-Perl-SDK-*.x86_64.tar.gz` under `/tmp` from
[https://my.vmware.com/group/vmware/downloads](https://my.vmware.com/group/vmware/downloads).
This requires creating of an account at VMware.

Build the RPM on the desired version of RHEL/CentOS:

        $ git clone https://github.com/marcindulak/VMware-vSphere-Perl-SDK-rpm-centos.git
        $ cd VMware-vSphere-Perl-SDK-rpm-centos
        $ cp -pf /tmp/VMware-vSphere-Perl-SDK-*.x86_64.tar.gz .
        $ CENTOSVER=7.2 vagrant up

Perform a basic test of the RPM installed in the guest, `vmware-cmd` should exit without errors:

        $ vagrant ssh -c "source /opt/VMware-vSphere-Perl-SDK/bin/VMware-vSphere-Perl-SDK.sh&& vmware-cmd --help"

The RPMS are created under `./$CENTOSVER`.
CENTOSVER available from https://atlas.hashicorp.com/puppetlabs are supported (6.6, 7.2).

When done, destroy the VM with::

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
