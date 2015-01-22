
#Judul : 
#Otomatisasi Proses Build dengan Apache Ant


Pembahasan

Petama kali kita perlu melakukan settingan terlebih dahulu pada PATH,menambah JAVA_HOME dan ANT_HOME Menambah  lokasi directory bin dari apache ant pada path, Menambah JAVA_HOME pada siatem variable agar dapat mengesekusi perintah ant.

Penjelasan dari isi dari build.xml :

Microsoft Windows XP [Version 5.1.2600]
(C) Copyright 1985-2001 Microsoft Corp.

C:\Documents and Settings\Student>  ant -version
Apache Ant version 1.7.1 compiled on June 27 2008
= Perintah untuk memeriksa instalan apache ant,  kalau sudah benar instalnya maka shell akan mengenali ant yang telah terinstal tersebut,hasilnya akan menampilkan tanggal,bulan, dan tahun instalanya seperti ini  : Apache Ant version 1.7.1 compiled on June 27 2008

C:\Documents and Settings\Student>  cd "My Documents"
= Perintah untuk menggunakan data pada memori yang berada di “My documen”
	
C:\Documents and Settings\Student\My Documents> cd Pertemuan1
= Perintah untuk menggunakan data pada memori dengan memanggil data pertemuan1

C:\Documents and Settings\Student\My Documents\Pertemuan1> dir
 Volume in drive C is SYSTEM
 Volume Serial Number is DC1E-75D2
 Directory of C:\Documents and Settings\Student\My Documents\Pertemuan1
11/10/2013  08:47<DIR>          .
11/10/2013  08:47<DIR>          ..
03/10/2011  09:19               558 build.xml
28/11/2012  18:13        10.920.710 apache-ant-1.8.2-bin.zip
11/10/2013  08:47<DIR>src
11/10/2013  08:47<DIR>          build
               2 File(s)     10.921.268 bytes
               4 Dir(s)   7.147.798.528 bytes free

C:\Documents and Settings\Student\My Documents\Pertemuan1> javac -sourcepath src-dbuild/classes/src/simpleant/HelloWorld.java
= Perintah javac diikuti oleh –sourcepath src, yang gunanya memberi  tahu java bahwa data yang akan dikompilasi di direktori src. Selanjutnya –d berguna untuk memberi tahu hasil kompilasi. 


C:\Documents and Settings\Student\My Documents\Pertemuan1> java -cp build/classes
 simpleant.HelloWorld
Hello World
= Perintah –cp (class path) yang mengikuti java berarti menunjukkan bahwa HelloWorld.java yang dikompilasi, class nya diletakkan di direktori classes. Kompilasi berhasil dilakukan jika “Hello World” muncul di layar.


C:\Documents and Settings\Student\My Documents\Pertemuan1>ant compile
Buildfile: build.xml
compile:
BUILD SUCCESSFUL
Total time: 0 seconds
= Kompilasi data yang dibuat menggunakan ant berhasil.

C:\Documents and Settings\Student\My Documents\Pertemuan1>ant jar
Buildfile: build.xml
jar:
      [jar] Building jar: C:\Documents and Settings\Student\My Documents\Pertemu
an1\build\jar\HelloWorld.jar
BUILD SUCCESSFUL
Total time: 0 seconds
= Pada  run bergantung pada  jar. run menjalankan perintah membuat direktori classes lalu ada proses dilakukan  yaitu mengakses file jar pada direktori jar.bergantung pada target compile yang sebelumnya dilakukan. jar akan membuat direktori jar yang digunakan untuk meletakkan file ,kalau berhasil akan seperti diatas.

C:\Documents and Settings\Student\My Documents\Pertemuan1>ant run
Buildfile: build.xml
run:
     [java] Hello World
BUILD SUCCESSFUL
Total time: 0 seconds
= Kompilasi menggunakan Ant run menjalankan  HelloWorld.jar ,mengakses pada  file jar pada direktori jar.kalau sukses maka akan muncul data [java] Hello World.

dan selesai cukup sekian.
