## ROUGE
### Base
which perl  
/usr/bin/perl  

### Step 1
git clone https://github.com/zingp/rouge.git  
cd rouge/ROUGE-1.5.5  

./runROUGE-test.pl  

if error:  
>>>>Cannot open exception db file for reading: data/WordNet-2.0.exc.db  
```
cd data
rm WordNet-2.0.exc.db
./WordNet-2.0-Exceptions/buildExeptionDB.pl ./WordNet-2.0-Exceptions ./smart_common_words.txt ./WordNet-2.0.exc.db
```
./runROUGE-test.pl  

### Step 2
pip uninstall pyrouge  
```
git clone https://github.com/bheinzerling/pyrouge.git
cd pyrouge
python setup.py install
pyrouge_set_rouge_path "yourpath/rouge/ROUGE-1.5.5"

python -m pyrouge.test
```

```
----------------------------------------------------------------------
Ran 11 tests in 6.649s

OK
```
