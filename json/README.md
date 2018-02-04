
Notes:
==============
```
Installing jsoncpp on Ubuntu
Ubuntu 16.04:
    sudo apt-get install libjsoncpp-dev
```


Example run
==============
```
~/CodeNuggets/json# make
Makefile:43: .depend: No such file or directory
rm -f ./.depend
g++ -g -O0 -std=c++11 -I. -I/usr/include/jsoncpp -MM ReadJsonCfg.cpp >  ./.depend;
g++ -g -O0 -std=c++11 -I. -I/usr/include/jsoncpp  -c -o ReadJsonCfg.o ReadJsonCfg.cpp
g++ ReadJsonCfg.o -L/usr/local/lib -ljsoncpp -o readjsoncfg
readjsoncfg compilation success!
:~/CodeNuggets/json# ./readjsoncfg 
______ cfg_root : start ______
{
        "Config" : 
        {
                "buffer-length" : 5000,
                "server-ip" : "10.10.10.20",
                "server-port" : "5555"
        },
        "Note" : "This is a cofiguration file"
}
______ cfg_root : end ________
______ Configuration ______
server-ip     :10.10.10.20
server-port   :5555
buffer-length :5000
```
