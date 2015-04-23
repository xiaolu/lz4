**Note : As Google Code is being closed, the new official LZ4 repository is now on Github** => https://github.com/Cyan4973/lz4

![http://sd-1.archive-host.com/membres/images/miniatures/182754578/SpeedCompare.png](http://sd-1.archive-host.com/membres/images/miniatures/182754578/SpeedCompare.png)
> LZ4 is a very fast lossless compression algorithm, providing compression speed at 400 MB/s per core, with near-linear scalability for multi-threaded applications. It also features an extremely fast decoder, with speed in multiple GB/s per core, typically reaching RAM speed limits on multi-core systems.

A high compression derivative, called LZ4\_HC, is also provided. It trades CPU time for compression ratio.

Quick comparison : single thread, Core i5-3340M @2.7GHz,
using  the [Open-Source Benchmark by m^2 (v0.14.2)](http://encode.ru/threads/1371-Filesystem-benchmark?p=33548&viewfull=1#post33548) compiled with GCC v4.6.1 on Linux Ubuntu 64-bits v11.10, using the [Silesia Corpus](http://sun.aei.polsl.pl/~sdeor/index.php?page=silesia)
```
Name		Ratio  C.speed D.speed
                        MB/s    MB/s
LZ4 (r101)	2.084	 422	1820
LZO 2.06	2.106	 414     600
QuickLZ 1.5.1b6	2.237	 373	 420
Snappy 1.1.0	2.091	 323	1070
LZF		2.077	 270	 570
zlib 1.2.8 -1	2.730	  65	 280
LZ4 HC (r101)   2.720     25    2080
zlib 1.2.8 -6	3.099	  21	 300
```

The LZ4 block compression format is detailed here : http://fastcompression.blogspot.com/2011/05/lz4-explained.html

For interoperability between multiple versions for streaming and file compression scenarios of any size, a frame format has been published : http://fastcompression.blogspot.fr/2013/04/lz4-streaming-format-final.html

**[Download latest release source code (zip or tar.gz format)](https://github.com/Cyan4973/lz4/releases/latest)**

License : the libraries (lz4, lz4hc and xxhash) are BSD license. The command line interface programs (lz4.exe, fullbench, fuzzer, datagen) are GPLv2.

---


### Interoperable LZ4 versions : ###

The following versions are provided for languages beyond the C reference version. They are conformant with the [LZ4 framing specification](http://fastcompression.blogspot.fr/2013/04/lz4-streaming-format-final.html) and are therefore interoperable.

  * **Javascript** : by Pierre Curto, at https://github.com/pierrec/node-lz4

  * **C++11** multi-threads : by Takayuki Matsuoka, at https://github.com/t-mat/lz4mt

  * **Python** : by Christopher Jackson, at https://github.com/darkdragn/lz4tools

  * **Delphi** binding : by Hanno Hugenberg, at https://github.com/Hugie/lz4-delphi

  * **Delphi** pure : by Jose Pascoa, at https://github.com/atelierw/LZ4Delphi

  * **Go** : by Pierre Curto, at https://github.com/pierrec/lz4

  * **Rust** : by Artem Navrotskiy, at https://github.com/bozaro/lz4-rs


### Other Source versions : ###

The following versions compress data blocks using LZ4 compression algorithm in multiple languages. Each version encapsulates the compressed result into its own header/frame format convention.

  * **Java** : by Adrien Grand, at https://github.com/jpountz/lz4-java

  * **Python** : by Steeve Morin, at http://pypi.python.org/pypi/lz4

  * **Perl** : by Gray, at http://search.cpan.org/dist/Compress-LZ4/

  * **C#** : by Milosz Krajewski, at http://lz4net.codeplex.com

  * **C# streaming** : by Phill Djonov, at https://github.com/pdjonov/Lz4Stream

  * **Go** : by Branimir Karadzic, at https://github.com/bkaradzic/go-lz4

  * **Ruby** : by Komiya Atsushi, at http://rubygems.org/gems/lz4-ruby

  * **PHP** : by Kamijo, at https://github.com/kjdev/php-ext-lz4

  * **Lua** : by Christophe Delord, at http://cdsoft.fr/bl/bonaluna.html

  * **Haskell** : by Mark Wotton, at http://hackage.haskell.org/package/lz4

  * **Erlang** : by Tetsuya Suzuki, at https://github.com/szktty/erlang-lz4

  * **Smalltalk** (Pharo) : by Mariano Martinez Peck, at http://smalltalkhub.com/#!/~marianopeck/LZ4/

  * **OCaml** : by Peter Zotov, at https://github.com/whitequark/ocaml-lz4

  * **Rust** : by Alex Crichton, at http://alexcrichton.com/rust-compress/compress/lz4/index.html

  * **8088 assembly** decoder, by Jim Leonard, at http://www.oldskool.org/pc/lz4_8088

  * **6502 & 65C02 assembly** decoder, by Peter Ferrie, at http://pferrie.host22.com/misc/appleii.htm

  * **Atari XL/XE assembly** decoder, by xxl, at http://xxl.atari.pl/?p=1524 [(\*)](https://www.youtube.com/watch?v=Su7Ui0cyRXM)

  * **65c816 assembly** decoder, by Olivier Zardini, at http://www.brutaldeluxe.fr/products/crossdevtools/lz4/index.html

  * **Z80 assembly** decoder, by Unknownloner, at http://www.cemetech.net/forum/viewtopic.php?t=11406



---

### What's new ? ###

**Future versions will only be available through Github ! See https://github.com/Cyan4973/lz4/releases/latest**

[r128](https://code.google.com/p/lz4/source/detail?r=128) : lz4cli sparse file support ([issue 155](https://code.google.com/p/lz4/issues/detail?id=155))

[r128](https://code.google.com/p/lz4/source/detail?r=128) : Restored lz4hc compression ratio

[r128](https://code.google.com/p/lz4/source/detail?r=128) : lz4frame supports skippable frames ([issue 150](https://code.google.com/p/lz4/issues/detail?id=150))

[r128](https://code.google.com/p/lz4/source/detail?r=128) : Visual project Directory

[r126](https://code.google.com/p/lz4/source/detail?r=126) : lz4frame API is now integrated into liblz4

[r125](https://code.google.com/p/lz4/source/detail?r=125) : New 32/64 bits, little/big endian and strict/efficient align detection routines

[r125](https://code.google.com/p/lz4/source/detail?r=125) : Small decompression speed improvement

[r124](https://code.google.com/p/lz4/source/detail?r=124) : New : LZ4 HC Streaming mode



---

### Executable binaries ###

  * **Windows** : by Yann Collet, at http://fastcompression.blogspot.fr/p/lz4.html

  * **Archlinux** : by Sébastien Luttringer, at https://www.archlinux.org/packages/community/x86_64/lz4/

  * **Debian** : by Nobuhiro Iwamatsu, at https://packages.debian.org/search?keywords=liblz4-1

  * **Ubuntu** : by Nobuhiro Iwamatsu, at https://launchpad.net/ubuntu/+source/lz4

  * **Gentoo** : by Gentoo community at https://packages.gentoo.org/package/app-arch/lz4

  * **OS-X** : via [Homebrew](http://brew.sh/), at https://github.com/Homebrew/homebrew/blob/master/Library/Formula/lz4.rb

  * **Amiga** : by Fredrik Wikstrom, at http://www.os4depot.net/index.php?function=showfile&file=library/misc/lz4_lib.lha


---

## LZ4 is used by ##

  * **Operating Systems** : <img src='http://static.commentcamarche.net/www.commentcamarche.net/faq/images/7283-linux-online-inc-s-.png' alt='Linux' height='50' /> [Linux](https://github.com/torvalds/linux) [(\*)](http://www.phoronix.com/scan.php?page=news_item&px=MTQwODY), <img src='http://blog.xen.org/wp-content/uploads/2014/01/Freebsd-logo.png' alt='FreeBSD' height='50' /> [FreeBSD](http://www.freebsd.org/) [(\*)](http://freebsdnow.blogspot.fr/2013/07/freebsd-92-feature-highlight-zfs-lz4.html), <img src='http://cloud.ohloh.net/attachments/38708/64x64-RGB_med.png' alt='Illumos' height='50' /> [Illumos](http://wiki.illumos.org/display/illumos/illumos+Home) [(\*)](http://wiki.illumos.org/display/illumos/LZ4+Compression), <img src='http://everycity.co.uk/wp-content/uploads/logos/supported/platforms/smartos_200_200.png' alt='SmartOS' height='50' /> [SmartOS](http://smartos.org/)

  * **File Systems** : <img src='https://dl.dropboxusercontent.com/u/59565338/Images/OpenZFS.png' alt='OpenZFS' height='50' />  [OpenZFS](http://www.open-zfs.org/wiki/Main_Page) [(\*)](http://www.open-zfs.org/wiki/Features#lz4_compression), [Hammer2](http://www.dragonflybsd.org/hammer/) [(\*)](http://lists.dragonflybsd.org/pipermail/commits/2013-September/198111.html), [SquashFS](http://squashfs.sourceforge.net/) [(\*)](http://www.phoronix.com/scan.php?page=news_item&px=MTY4OTc), [LessFS](http://www.lessfs.com/wordpress/) [(\*)](http://www.lessfs.com/wordpress/?p=688), <img src='http://leo-project.net/leofs/assets/logos/leofs-logo-blk-2.png' alt='LeoFS' height='50' /> [LeoFS](http://leo-project.net/leofs/) [(\*)](http://fr.slideshare.net/rakutentech/scaling-and-high-performance-storage-system-leofs/36), [Grub](http://www.gnu.org/software/grub/)

  * **Big Data** : <img src='http://courses.coreservlets.com/images/hadoop-logo.png' alt='Hadoop' height='50' /> [Hadoop](http://hadoop.apache.org/) [(\*)](https://issues.apache.org/jira/browse/HADOOP-7975), <img src='http://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Cassandra_logo.svg/279px-Cassandra_logo.svg.png' alt='Cassandra' height='50' /> [Cassandra](http://cassandra.apache.org/) [(\*)](http://www.slideshare.net/jbellis/london-dublin-cassandra-20/20), [Hbase](http://hbase.apache.org/) [(\*)](https://issues.apache.org/jira/browse/HBASE-5838), [Rarelogic](http://www.rarelogic.com/), <img src='http://upload.wikimedia.org/wikipedia/commons/e/ea/Spark-logo-192x100px.png' alt='Spark' width='70' />[Spark](http://spark.apache.org/) [(\*)](https://github.com/apache/spark/pull/1416), [Hustle](https://github.com/chango/hustle) [(\*)](https://groups.google.com/forum/#!topic/lz4c/hcoN8c-OK4Q)

  * **Search Engine** : <img src='http://cloud.ohloh.net/attachments/45788/lucene_med_med.png' alt='Lucene' height='50' /> [Lucene](http://lucene.apache.org/) [(\*)](http://blog.jpountz.net/post/35667727458/stored-fields-compression-in-lucene-4-1), <img src='http://nickveenhof.github.io/devdays_solr_wizardry/images/solr_logo_rgb.png' alt='Solr' height='50' /> [solr](http://lucene.apache.org/solr/) [(\*)](http://www.searchbox.com/solr-4-2-vs-solr-4-1-compressed-term-frequency-vectors/), [Scalyr](https://www.scalyr.com/) [(\*)](http://blog.scalyr.com/2014/05/searching-20-gbsec-systems-engineering-before-algorithms/#comment-115), <img src='http://kafka.apache.org/images/kafka_logo.png' alt='kafka' height='50' />[Kafka](http://kafka.apache.org/) [(\*)](https://issues.apache.org/jira/browse/KAFKA-1456)

  * **Database** : <img src='http://dev.mysql.com/common/logos/logo-mysql-110x57.png' alt='MySQL' width='80' /> [MySQL](http://dev.mysql.com/) [(\*)](http://dev.mysql.com/doc/mysql-enterprise-backup/3.10/en/backup-compression-options.html), [Tokudb](http://www.tokutek.com/products/tokudb-for-mysql/), [Delphix](http://www.delphix.com/products/overview/) [(\*)](http://docs.delphix.com/display/DOCS32/What's+New+in+Delphix+3.2#What'sNewinDelphix3.2-ReplicationEnhancements), [infiniSQL](http://www.infinisql.org/) [(\*)](http://www.infinisql.org/docs/guide/#idp37036608), <img src='http://cognitiones.kantel-chaos-team.de/webworking/db/images/rocksdb-logo.png' alt='RocksDB' height='50' />  [RocksDB](http://rocksdb.org/) [(\*)](https://github.com/facebook/rocksdb/pull/74), <img src='http://ih1.redbubble.net/image.22493834.2423/fc,220x200,white.u1.jpg' alt='OlegDB' height='50' /> [OlegDB](https://olegdb.org/) [(\*)](https://olegdb.org/blog/0004_LZ4.html)

  * **Games** : <img src='https://lh4.googleusercontent.com/-QxT7qF3nu0g/AAAAAAAAAAI/AAAAAAAAAAA/g5dy7Cpe1yI/s48-c-k/photo.jpg' alt='BF4' /> [Battlefield 4](http://www.battlefield.com/battlefield-4) [(\*)](https://twitter.com/bionicbeagle/status/372692756012859392), <img src='http://gaygamer.net/images/GW2_Primary_Textured_FC.png' alt='GW2' height='50' /> [Guild Wars 2](https://www.guildwars2.com/fr/) [(\*)](https://twitter.com/bkaradzic/status/466083995642376192), <img src='http://upload.wikimedia.org/wikipedia/de/6/60/Crytek_logo.png' alt='Crytek' width='80' /> [Crytek](http://www.crytek.com/) [(\*)](http://slidegur.com/doc/24764/ryse_siggraph_aug_2014_axel_gneiting_real-time), <img src='http://uk.playstation.com/media/ArozIyTc/163/282291.jpg' alt='1000TC' height='50' />   [1000 Tiny Claws](http://www.pspminis.com/7651/1000-tiny-claws-review-yar-thar-be-lots-of-insects/) [(\*)](http://fastcompression.blogspot.fr/2011/10/lz4-in-commercial-application.html)

  * **Graphics** : <img src='http://upload.wikimedia.org/wikipedia/fr/thumb/2/21/Nvidia_logo.svg/220px-Nvidia_logo.svg.png' alt='nVidia' height='50' /> [nVidia](http://www.nvidia.com/) [(\*)](http://us.download.nvidia.com/XFree86/Linux-x86/343.13/README/acknowledgements.html), <img src='http://www.enlightenment.org/p/index/d/logo.png' alt='Enlightenment' height='50' />  [Enlightenment](http://www.enlightenment.org/) [(\*)](http://git.enlightenment.org/legacy/eet.git/commit/src/lib/Eet.h?h=master&id=7c73c5562269b07188c1a8511fb05d7405381436), <img src='http://xpra.org/icons/xpra-logo.png' alt='Xpra' height='50' /> [Xpra](https://www.xpra.org/) [(\*)](https://www.xpra.org/trac/wiki/PacketEncoding), <img src='http://www.cartoonbrew.com/wp-content/uploads/open_vdb_logo_web-e1344041308558.png' alt='OpenVDB' height='50' /> [OpenVDB](http://www.openvdb.org/) [(\*)](http://www.openvdb.org/documentation/doxygen/changes.html#v3_0_0_changes), [Scaplib](http://scap.codeplex.com/), [kanzi](https://code.google.com/p/kanzi/) [(\*)](https://code.google.com/p/kanzi/wiki/SnappyCodec)

  * **Network** : <img src='http://hardwaredenlk.files.wordpress.com/2013/04/freenas_logo_twitter.jpg' alt='freeNAS' height='50' /> [freeNAS](http://www.freenas.org/) [(\*)](https://bugs.freenas.org/issues/3872), <img src='http://www.tharunpkarun.com/data/uploads/2012/05/openvpn1.png' alt='openVPN' height='50' /> [openVPN](http://openvpn.net/) [(\*)](http://openvpn.net/index.php/component/content/article/119-faq-openvpn-client/533-connect-android-release-notes.html), <img src='https://dl.dropboxusercontent.com/u/59565338/Images/Netty.png' alt='Netty' height='50' />[Netty](http://netty.io/) [(\*)](https://github.com/netty/netty/pull/2739), <img src='http://dovecot.org/dovecot.gif' alt='dovecot' width='70' /> [dovecot](http://dovecot.org/) [(\*)](http://news.softpedia.com/news/Dovecot-2-2-11-Now-Comes-with-LZ4-Compression-Support-426327.shtml), <img src='http://www.virtualhere.com/sites/default/files/img2_0.png' alt='virtualHere' height='50' />[virtualHere](http://www.virtualhere.com/) [(\*)](http://www.virtualhere.com/client_license)

  * **Storage** : <img src='http://openvirtualizationalliance.org/images/uploads/member_orgs/datastax_logo_x.png' alt='Datastax' height='50' /> [DataStax](http://www.datastax.com/) [(\*)](http://www.datastax.com/documentation/datastax_enterprise/4.0/datastax_enterprise/compression.html), <img src='http://www.silicon.fr/wp-content/uploads/2012/12/Nimble-Storage.jpeg' alt='Nimble Storage' height='50' /> [Nimble Storage](http://www.hybrid-san.co.uk/) [(\*)](https://twitter.com/NimbleFacts/status/444404208545325056), <img src='http://www.silicon.fr/wp-content/uploads/2013/02/Nexenta-logo.png' alt='Nexenta' height='50' /> [Nexenta](http://www.nexenta.com/) [(\*)](http://www.nexenta.com/company/media/press-releases/nexenta-delivers-next-generation-software-defined-storage-solutions-0), [K2 Spear](http://kaminario.com/flash-array/) [(\*)](http://kaminario.com/flash-array/features.php#inline_compression), [Syneto OS](http://syneto.net/) [(\*)](http://syneto.net/blog/2014/02/syneto-storage-os-2-14-released/)

  * **Caching** : [Zram](http://en.wikipedia.org/wiki/ZRam) [(\*)](http://kernelnewbies.org/Linux_3.15#head-52af9ef123b7c0792b09a1a0222fdc8c21ab5d4c), <img src='http://docs.hhvm.com/images/og.png' alt='HHVM' height='50' /> [HHVM](http://hhvm.com/) [(\*)](https://github.com/hhvm/hhvm-third-party/tree/master/lz4), [PHP Zend Optimizer](http://www.zend.com/‎)

  * **Other** : <img src='https://mozorg.cdn.mozilla.net/media/img/styleguide/identity/firefox/guidelines-logo.png?2013-06' alt='mozilla firefox' height='50' />[Mozilla Firefox](https://www.mozilla.org/) [(\*)](http://blog.bonardo.net/2014/05/28/bookmarks-backups-redesign), <img src='https://www.bareos.org/assets/images/9/Logo_signet_64x64-4e199499.png' alt='bareos' height='50' />[Bareos](https://www.bareos.org/en/) [(\*)](http://www.bareos.org/en/HOWTO/articles/new-in-version-1320.html), <img src='http://upload.wikimedia.org/wikipedia/commons/6/68/Gtkwave_256x256x32.png' alt='GTKWave' height='50' /> [GTKWave](http://gtkwave.sourceforge.net/), [Blosc](https://github.com/Blosc/c-blosc), [Facebook's Mercurial](https://bitbucket.org/facebook/lz4revlog), [Nippy](https://github.com/ptaoussanis/nippy), [systemd](http://www.freedesktop.org/wiki/Software/systemd) [(\*)](http://lists.freedesktop.org/archives/systemd-devel/2014-August/022295.html)

If you know more of them, and feel they should be mentioned in this list, let us know. The easiest way to get in touch is via the [Public discussion forum](http://groups.google.com/group/lz4c).


---

## Public discussion ##

Public discussion forum is here: http://groups.google.com/group/lz4c

Post bug reports or feature request to the Issue Tracker: http://code.google.com/p/lz4/issues/list