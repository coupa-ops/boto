1. Clone the repository - `git clone git@github.com:coupa-ops/boto.git`
2. Checkout branch 2.45.0_fips - `git checkout 2.45.0_fips`
3. Run command - `python setup.py bdist_rpm --release=5 --provides=python-boto`
4. It will build the module and generate rpm package at `$PWD/dist/` as 
``` 
[parvez_kazi@dev954dbm boto]$ ls -1 dist
python2-boto-2.45.0-5.noarch.rpm
python2-boto-2.45.0-5.src.rpm
python2-boto-2.45.0.tar.gz
```
5. Install the rpm to test, `sudo rpm -Uvh dist/python2-boto-2.45.0-5.noarch.rpm`
6. Patch file is [here](./boto_2.45.0_fips.patch)