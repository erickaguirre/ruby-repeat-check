ruby-repeat-check
=================

Run ruby's make check repetedly

## Usage

Build ruby.

    git clone https://github.com/akr/ruby-repeat-check.git
    cd ruby-repeat-check

    # build ruby trunk in a directory ("o0" here but other names are ok)
    mkdir o0
    cd o0
    prefix=`pwd`
    svn co http://svn.ruby-lang.org/repos/ruby/trunk ruby
    cd ruby
    autoconf
    ./configure --prefix="$prefix" --disable-install-doc optflags=-O0
    make all install
    cd ../..

    ./loop >& z.log

Watch `error/*.log` in another terminal.

