
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
 > pwd
/root/CodeNuggets/json/config_read
 > ls -l
total 16
-rw-r--r-- 1 root root  689 Feb  4 02:30 Makefile
-rw-r--r-- 1 root root  911 Feb  4 02:38 README.md
-rw-r--r-- 1 root root 1207 Feb  4 02:29 ReadJsonCfg.cpp
-rw-r--r-- 1 root root  175 Feb  4 02:15 cfg.json
 > make
Makefile:43: .depend: No such file or directory
rm -f ./.depend
g++ -g -O0 -std=c++11 -I. -I/usr/include/jsoncpp -MM ReadJsonCfg.cpp >  ./.depend;
g++ -g -O0 -std=c++11 -I. -I/usr/include/jsoncpp  -c -o ReadJsonCfg.o ReadJsonCfg.cpp
g++ ReadJsonCfg.o -L/usr/local/lib -ljsoncpp -o readjsoncfg
readjsoncfg compilation success!
 > ./readjsoncfg 
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
