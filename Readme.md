This project documents getting GNU toolchain compiling and deploying sample robot code.  Tested 9/7/2013 on Ubuntu 13.04 amd64.
updated to Ubuntu 13.10 12/10/2013

Most information from:
    http://firstforge.wpi.edu/sf/wiki/do/viewPage/projects.c--11_toochain/wiki/BinaryInstall


Here are the commands used:


    # (as root)
    echo "deb http://debian.repo.frc.s3.amazonaws.com jessie main" >> /etc/apt/sources.list
    wget -O - http://debian.repo.frc.s3.amazonaws.com/rbmj.gpg.key | apt-key add -
    apt-get update
    apt-get install gcc-powerpc-wrs-vxworks frc-buildscripts wpilib

    export WIND_BASE=/usr/powerpc-wrs-vxworks/wind_base
    cd build
    frcmake ..
    make
    make deploy

