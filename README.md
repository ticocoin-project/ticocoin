Copyright (c) 2009-2020 Bitcoin Developers
Copyright (c) 2011-2020 Ticocoin Developers

Que es Ticocoin?
-----------------------

Ticocoin es una criptomoneda que utiliza scrypt como algoritmo de trabajo similar a Bitcoin y Litecion.
 - Block targets (Consigue el bloque) ~ de 5 minutos
 - Halvin a los 50k Bloques (reduccion de recompenza a la mitad)
 - ~ 4 millones de monedas en total


Ticocoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 5 minute block targets
 - subsidy halves in 50k blocks
 - ~4 million total coins

Recompensa Mineros.
  - 40 Coins (Monedas)	


License - Licencia
----------------------------

Ticocoin se lanza bajo los términos de la licencia MIT. Vea `COPYING` para más
información o consulte http://opensource.org/licenses/MIT.

Ticocoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.



Informacion de la moneda - Info Coin
----------------------------------------------------------

Puede Consultar la web: http://ticocoin.cf/
Tambien explorar las transacciones en: http://explorer.ticocoin.cf/
Crear tu propia billetera: https://wallet.ticocoin.cf/

You can consult the web: http://ticocoin.cf/
Also explore transactions at: http://explorer.ticocoin.cf/
Create your own wallet: https://wallet.ticocoin.cf/


Importante
----------------------------------------------------------

Ver en todo momento la Hoja Magica


Serie de videos `YOUTUBE` --->




Para compilar se necesita tener:


https://github.com/devrandom/gitian-builder

sudo bin/make-base-vm --precise --archamd64  ---> esto escribirlo en la consola en la carpeta y continuar con lo ultimo que dice la hoja magica


Build base VM:
 
bin/make-base-vm --lxc --arch amd64 --suite precise
 
Dependencies (make sure this is done in the gitian-builder directory):
 
mkdir -p inputs; cd inputs/
 
wget 'http://miniupnp.free.fr/files/download.php?file=miniupnpc-1.9.20140401.tar.gz' -O 'miniupnpc-1.9.20140401.tar.gz'
wget 'https://www.openssl.org/source/openssl-1.0.1k.tar.gz'
wget 'http://download.oracle.com/berkeley-db/db-4.8.30.NC.tar.gz'
wget 'https://www.zlib.net/fossils/zlib-1.2.8.tar.gz'
wget 'ftp://ftp.simplesystems.org/pub/libpng/png/src/history/libpng16/libpng-1.6.8.tar.gz'
wget 'http://fukuchi.org/works/qrencode/qrencode-3.4.3.tar.bz2'
wget 'http://downloads.sourceforge.net/project/boost/boost/1.55.0/boost_1_55_0.tar.bz2'
wget 'https://download.qt.io/archive/qt/4.8/4.8.5/qt-everywhere-opensource-src-4.8.5.tar.gz'
wget 'https://svn.boost.org/trac/boost/raw-attachment/ticket/7262/boost-mingw.patch' -O boost-mingw-gas-cross-compile-2013-03-03.patch
 
Building depencies (in gitian-builder, replace instances of 'funcoin' with whatever you named your clone):
 
./bin/gbuild ../funcoin/contrib/gitian-descriptors/boost-win32.yml
mv build/out/boost-*.zip inputs/
 
./bin/gbuild ../funcoin/contrib/gitian-descriptors/deps-win32.yml
mv build/out/bitcoin*.zip inputs/
 
./bin/gbuild ../funcoin/contrib/gitian-descriptors/qt-win32.yml
mv build/out/qt*.zip inputs/
 
Compile your coin (remember tag & name change):
 
./bin/gbuild --commit funcoin=v0.8 ../funcoin/contrib/gitian-descriptors/gitian-win32.yml


Clonar gitian builder ----------

git clone https://github.com/devrandom/gitian-builder.git



Repositorios para compilar billetera windows -------

https://www.openssl.org/source/old/1.0.1/openssl-1.0.1i.tar.gz

http://download.oracle.com/berkeley-db/db-4.8.30.NC.tar.gz

http://miniupnp.free.fr/files/download.php?file=miniupnpc-1.9.20140401.tar.gz

http://fossies.org/linux/misc/zlib-1.2.8.tar.gz

http://sourceforge.net/projects/libpng/files/libpng16/older-releases/1.6.8/libpng-1.6.8.tar.gz/download

https://fukuchi.org/works/qrencode/qrencode-3.4.3.tar.bz2

https://sourceforge.net/projects/boost/files/boost/1.55.0/boost_1_55_0.tar.bz2/download?use_mirror=pilotfiber&r=http%3A%2F%2Fwww.boost.org%2Fusers%2Fhistory%2Fversion_1_55_0.html&use_mirror=internode

https://svn.boost.org/trac/boost/raw-attachment/ticket%2F7262/boost-mingw.patch

http://wtogami.fedorapeople.org/boost-mingw-gas-cross-compile-2013-03-03.patch

https://download.qt.io/archive/qt/4.8/4.8.5/qt-everywhere-opensource-src-4.8.5.tar.gz


sudo bin/make-base-vm --precise --archamd64








