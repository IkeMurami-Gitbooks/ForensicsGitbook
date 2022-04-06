# GZIP/ZLIB

```
Для zlib:
CMF | FLG
0x78 | 0x01 - No Compression/low
0x78 | 0x9C - Default Compression
0x78 | 0xDA - Best Compression 
```

```
ZLIB/GZIP headers:
Level | ZLIB | GZIP
1 | 78 01 | 1F 8B
2 | 78 5E | 1F 8B
3 | 78 5E | 1F 8B
4 | 78 5E | 1F 8B
5 | 78 5E | 1F 8B
6 | 78 9C | 1F 8B
7 | 78 DA | 1F 8B
8 | 78 DA | 1F 8B
9 | 78 DA | 1F 8B
```
