# Install VPFIT on Mac

Assuming the following has been done: 

```bash
brew install libpng
brew install cfitsio
brew install pgplot
brew install gcc
```
Run

```bash
wget http://www.ast.cam.ac.uk/~rfc/vpfit10.2.tar.gz
mkdir vpfit10.2
cd vpfit10.2
tar -xvzf ../vpfit10.2.tar.gz
mv Makefile Makefile.sav
```

At this point you might want need to double check the directories of `cfitsio` and `pgplot`

 - todo find a programatic way to get the following paths right

```bash
sed -e 's%/sw/lib/libcfitsio.a%/usr/local/Cellar/cfitsio/3.390/lib/libcfitsio.a%g' \
    -e 's%-L/sw/lib/pgplot%-L/usr/local/Cellar/pgplot/5.2.2_1/lib%g' \
    -e 's%-L/sw/lib/%%g' \
    -e 's%-laquaterm%%g' \
    Makefile.sav > Makefile

make vpmac

mv vpfit /usr/local/bin/
```
