# How to mine GOTH on Linux (Ubuntu)  

`sudo apt-get update`  
`sudo apt-get install libcurl4-openssl-dev git build-essential autotools-dev autoconf libcurl3 libcurl4-gnutls-dev`  
`mkdir ~/miner; cd ~/miner`  
`git clone https://github.com/pooler/cpuminer; cd cpuminer`  

### Compile and install the miner

```
./autogen.sh
CFLAGS="-march=native" ./configure
make
sudo make install
```  
### Start mining
`minerd -o stratum+tcp://gothpool.gothcoin.cc:3256 -u WALLET -p 1234`
