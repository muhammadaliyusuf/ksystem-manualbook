# ksystem-manualbook

---------------------------------------------------------------------------------------------

## INSTALL KSYSTEM DARI AWAL [DAY-2 04/06/25]
(file:///home/ksystem/Documents/Tutor/kstutor/c4.html)
(/home/ksystem/Documents/Tutor/ksweb_dtubahver20.txt)

### ksystem.co > Klik Kiri di Logo KSYSTEM > Download:
- parsegen[yy-mm-dd]a.tgz
- ksystem[yy-mm-dd]a.wt
- ksresource[yy-mm-dd].tgz
- prgweb[yy-mm-dd].tgz
- getsetup.sh

### Jalankan command:
> bash Downloads/getsetup.sh (sesuaikan letak file)
> setup2/setup ksystem
> masukkan password: 12 (sesuaikan dgn pw saat install ubuntu)
> tar xvfz parsegen
> tar xvfz ksresources
> tar xvfz prgweb__
> cp ksystem__.wt ksystem.wt
> runwt
> browser > localhost

> create ks_std;
> use ks_std;
> source ks_std[yy-mm-dd].sql;

---------------------------------------------------------------------------------------------

## UPDATE KSYSTEM

### File Requirement:
- parsegen[yy-mm-dd]a.tgz (file update)
- ksystem[yy-mm-dd]a.wt (file update)

### Jalankan command:
> docker stop ks
> tar xvfz parsegen
> cp ksystem__.wt ksystem.wt
> docker start ks
> kspar all
> kspar -x9999
> ksgen
> ksgen x-9999
> runwt
= Jika berhasil maka Klangnya berubah sesuai versi file-nya (localhost -> klik kiri logo ksystem -> klik About Ksystem)

---------------------------------------------------------------------------------------------

## UPDATE STRUKTUR

### File Requirement:
- PrgWeb[yy-mm-dd].tgz (file update)

### Jalankan command:
> tar xvfz PrgWeb__.tgz
> mysql -uroot
> DROP database ks_std;
> CREATE database ks_std;
> use ks_std;
> source ks_std250511.sql;

> ksh bin/ksubhsql ks_umum
> mysql -uroot
> use ks_umum;
> source ubhsql.txt;

> browser > localhost > jika muncul popup selain login, jalankan:
> use ks_umum;
> DROP table ahm;
> ksh bin/ksubhsql ks_umum
> docker restart ks
> runwt 

---------------------------------------------------------------------------------------------
