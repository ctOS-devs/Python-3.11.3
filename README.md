# Инструкция по сборке
1. Отредактировать `Modules/Setup` для доп.сборки (в репо уже настроено +-)
2. Создать папку: `mkdir INSTALLED`
3. Конфигурировать сборку: `./configure LDFLAGS="-static -static-libgcc" CPPFLAGS="-fPIC -static" --disable-shared --prefix=$(pwd)/INSTALLED/ --enable-optimizations`
4. Собрать в 8 потоков: `make -j 8`
5. Установить: `make install -j 8`
6. УДАЛИТЬ ГОВНО: `rm -rf INSTALLED/lib/python3.11/test`

## Успешно собранные библиотеки:
```
_asyncio              _bisect               _blake2            
_bz2                  _codecs_cn            _codecs_hk         
_codecs_iso2022       _codecs_jp            _codecs_kr         
_codecs_tw            _contextvars          _crypt             
_csv                  _ctypes               _datetime          
_decimal              _elementtree          _hashlib           
_heapq                _json                 _lsprof            
_lzma                 _md5                  _multibytecodec    
_multiprocessing      _opcode               _pickle            
_posixshmem           _posixsubprocess      _queue             
_random               _sha1                 _sha256            
_sha3                 _sha512               _socket            
_ssl                  _statistics           _struct            
_typing               _zoneinfo             array              
audioop               binascii              cmath              
fcntl                 grp                   math               
mmap                  ossaudiodev           pyexpat            
readline              resource              select             
spwd                  syslog                termios            
unicodedata           zlib     
```

## Не успешно собранные библиотеки:
```
_ctypes_test          _curses               _curses_panel      
_gdbm                 _testbuffer           _testcapi          
_testclinic           _testimportmultiple   _testinternalcapi  
_testmultiphase       _uuid                 _xxsubinterpreters 
_xxtestfuzz           nis                   xxlimited          
xxlimited_35                     
```
