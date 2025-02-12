# decode protobuf
https://brutecat.com/articles/leaking-youtube-emails
```
$ echo -n "Q2lrcUp3b1lWVU5vY3pCd1UyRkZiMDVNVmpSdFpYWkNSa2RoYjB0QkVnc3pObGx1VmpsVFZFSnhZMUFBV0FGaUx3b1ZNVEV6T1RBM05EWTJOVE0zTmpjd016Y3dOVGt3RWhaVFJTMWhXVTlpTFhWRFp6QTFPWEZJVW1selgyOTNjQUElM0Q=" | base64
 -d | sed 's/%3D/=/g' | base64 -d | protoc --decode_raw
1 {
  5 {
    1: "UChs0pSaEoNLV4mevBFGaoKA"
    2: "36YnV9STBqc"
  }
}
10: 0
11: 1
12 {
  1: "113907466537670370590"
  2: "SE-aYOb-uCg059qHRis_ow"
}
14: 0
```
