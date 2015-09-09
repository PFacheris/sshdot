## Usage

sshdot works just like sshrc, which in turn, works just like ssh - but it also sources the ~/.sshrc on your local computer after logging in remotely.
sshdot differs from sshrc in that it has no size restrictions for the files you copy to the remote machine. Want to include your entire .vim folder? Go right ahead.

    $ echo "echo welcome" > ~/.sshrc
    $ sshrc me@myserver
    welcome

    $ echo "alias ..='cd ..'" > ~/.sshrc
    $ sshdot me@myserver
    $ type ..
    .. is aliased to `cd ..'

## Installation

#### Everything

    $ wget https://raw.githubusercontent.com/pfacheris/sshdot/master/sshdot &&
    chmod +x sshdot &&
    sudo mv sshdot /usr/local/bin #or anywhere else on your PATH

## More Info

See (https://github.com/Russell91/sshrc) for more info on the project this is based on.
