# What is this spec?

This repository contains specs for the high availability cluster resource manager pacemaker (http://clusterlabs.org/) to be built on Amazon AWS infrastructure based on CentOS distributions.

# What is the current version?

Pacemaker 1.1.9
PCS 0.9.37
Libqb 0.14.4

# How to build?

Move the repository contents for an directory like that:

    /home/ec2-user/packaging/pacemaker

And run rpmbuild:

    cd /home/ec2-user/packaging/pacemaker && rm -rf BUILDROOT/* BUILD/* RPMS/x86_64/* RPMS/noarch/* && cd SPECS/ && rpmbuild -ba --buildroot=/home/ec2-user/packaging/pacemaker/BUILDROOT --define='_topdir /home/ec2-user/packaging/pacemaker' --sign pacemaker.spec

