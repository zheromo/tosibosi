==Algorithm
http://dyagilev.org/blog/2012/03/23/consistent-hashing/

https://jaidayo.livejournal.com/2645.html

https://habr.com/ru/company/miro/blog/535266/

==
https://github.com/lithammer/python-jump-consistent-hash

https://gist.github.com/badboy/6267743

==Python
https://github.com/ultrabug/uhashring
https://docs.openstack.org/swift/latest/ring_background.html


def hash\_djb2(s):  
    hash = 5381  
 for x in s:  
        hash = ((hash << 5) + hash) + ord(x)  
    return hash & 0xFFFFFFFF  
  
  
def hash\_sdbm(s):  
    hash = 0  
 for x in s:  
        hash = ((hash << 16) + (hash << 6) + ord(x) - hash) & 0xFFFFFFFF  
 return hash  
  
  
def hash\_lose(s):  
    hash = 0  
 for x in s:  
        hash += ord(x)  
    return hash

FNV https://github.com/znerol/py-fnvhash

crc16
crc32 
Murmur2/Murmur3
