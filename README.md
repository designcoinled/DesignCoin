Design Coin (SIGN) integration/staging repository
======================================


Quick installation of the Design Coin daemon under linux.

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/designcoinled/DesignCoin.git
    cd DesignCoin
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip designcoind
    sudo strip designcoin-cli
    sudo strip designcoin-tx
    cd ..

Running the daemon:

    designcoind 

Stopping the daemon:

    designcoin-cli stop

Demon status:

    designcoin-cli getinfo
    designcoin-cli mnsync status



### Coin Specs
<table>
<tr><td>Algo</td><td>Quark</td></tr>
<tr><td>Block Time</td><td>60 Seconds</td></tr>
<tr><td>Max Coin Supply</td><td>21.000.000 SIGN</td></tr>
<tr><td>Premine</td><td>400.000 SIGN</td></tr>
<tr><td>Maturity</td><td>30</td></tr>
<tr><td>DefaultPort</td><td>21566</td></tr>
<tr><td>RPCPort</td><td>21565</td></tr>
<tr><td>MN collateral</td><td>3000 SIGN</td></tr>
<tr><td>Reward split</td><td>85%(MN) / 15%(POS)</td></tr>
</table>


### Table of Block Rewards

<table>
<th>Block Height</th><th>Reward</th>
<tr><td>0 - 7000</td><td>2 SIGN</td></tr>
<tr><td>7001 - 70000</td><td>20 SIGN</td></tr>
<tr><td>70001 - 1700000</td><td>10 SIGN</td></tr>
<tr><td>170001 - 3000000</td><td>5 SIGN</td></tr>
<tr><td>3000001 +</td><td>2 SIGN</td></tr>
</table>



---
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
