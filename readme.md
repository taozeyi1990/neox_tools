# Neox Model Converter & EXPK/NXPK Extractor

python version is 3!

Step 0
```
pip install numpy transformations pymeshio tqdm pyqt5 moderngl
```
If you are in China, please use ...
```
pip install numpy transformations pymeshio tqdm pyqt5 moderngl -i https://pypi.douban.com/simple
```
Step 1
```
python extractor.py expk_file_path
```
example:
```
python extractor.py hero1.npk
```
if you'll unpack Onmyoji game.
you should first rename these files like below:

res.npk.0 -> res.npk.00

res.npk.1 -> res.npk.01

...

res.npk.10 -> res.npk.10

...

res.npk.14 -> res.npk.14


then:
```
copy/b res.npk.* res.npk
python extractor.py res.npk
```

Step 2
```
python converter.py mesh_file_path
```
example:
```
python converter.py hero1/00390823.mesh
```
if you want obj format:
```
python converter.py mesh_file_path --mode obj
```
if you want iqe format:
```
python converter.py mesh_file_path --mode iqe
```

You can check this page for update:
https://github.com/zhouhang95/neox_tools

Step 3
```
python main.py
```
File -> Load Unpack Folder


then select the generated folder after unpacking
