### LOW-LATENCY SPREAD MARKET MAKER

This simple Spread based MARKET MAKER demonstrate how to develop
High Frequency trading automation using advanced C++ features and
flexible archichture that can be easy deployed on multi exchanges or brokers


##### Supported OS

* Linux, Windows

##### Available exchanges/brokers

* Binance

##### BUILD SPMAKER

```
scl enable devtoolset-9 bash
git clone https://github.com/silvadom/spmaker.git
cd spmaker
cmake . -DG3LOG_ROOT=/usr/local/g3log -DJSON_ROOT=/usr/local/json
make install
```

Others CMAKE libraries root path options:
```
-DJSON_ROOT=path_to_json
-DOPENSSL_ROOT=path_to_openssl
-DG3LOG_ROOT=path_to_g3log
-DONETBB_ROOT=path_to_onetbb
-DBOOST_ROOT=path_to_boost
-DCPR_ROOT=path_to_cpr
```

##### RUN SPMAKER

- add binance API KEY and SECRET in build/configs/connector.config

```
cd build/bin
./spmaker --risk 1000 --capital 5000 --threads 8 --timeout 2 -v 1
```

