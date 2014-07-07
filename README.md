# ruby-install port for FreeBSD

## Quickstart (install)

    cd /tmp
    git clone https://github.com/steakknife/ruby-install-freebsd
    cd ruby-install-freebsd
    ./install # installs to /usr/ports/lang/ruby-install
    rm -rf /tmp/ruby-install-freebsd
    cd /usr/ports/lang/ruby-install
    [sudo or su -c] make install clean

if git is not already installed, run:

    pkg install git


## Uninstall

    [sudo or su -c] pkg remove ruby-install


## Notes

Portsnap or anything that updates/replaces /usr/ports may/will overwrite this.


## Support

Tested on FreeBSD 10.0/amd64 only


## License

BSD 2-clause license


## Copyright

Copyright (c) 2014 Barry Allard
