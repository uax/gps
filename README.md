# GPS Convert
* WGS-84：是国际标准，GPS坐标（Google Earth使用、或者GPS模块）
* GCJ-02：中国坐标偏移标准，Google Map、高德、腾讯使用
* BD-09：百度坐标偏移标准，Baidu Map使用
## 使用说明
``` php
use GPS\Convert;
```
**WGS-84 to GCJ-02:**
``` php
Convert.gcj_encrypt();
```
**GCJ-02 to WGS-84 粗略:**
``` php
Convert.gcj_decrypt();
```
**GCJ-02 to WGS-84 精确(二分极限法):**
``` php
GSP.gcj_decrypt_exact();
```
**GCJ-02 to BD-09:**
``` php
Convert.bd_encrypt();
```
**BD-09 to GCJ-02:**
``` php
Convert.bd_decrypt();
```
**求距离:**
``` php
Convert.distance();
```
**注意：**本算法 gcj算法、bd算法都非常精确，已经测试通过。（BD转换的结果和百度提供的接口精确到小数点后4位），请放心使用。