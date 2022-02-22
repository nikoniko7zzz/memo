<!-- omit in toc -->
# PyCaretを使ってPythonの機械学習を楽に実装！
『YOUTUBE いまにゅのプログラミング塾』を参考にやってみた

- [環境](#環境)
- [参考にしたサイト](#参考にしたサイト)

## 環境
mac
vscode .ipynb

## 参考にしたサイト
- [いまにゅのプログラミング塾　YOUTUBE](https://www.youtube.com/watch?v=35pS0YgMsAo)
- [詳しく書いてあるサイト](https://aiacademy.jp/media/?p=954)

```python
pip install pycaret
```

```python
from pycaret.regression import *
```

エラーが出た
```python
ImportError: Numba needs NumPy 1.20 or less
```
対処法　[参考サイトリンク](https://stackoverflow.com/questions/70148065/numba-needs-numpy-1-20-or-less-for-shapley-import)
```python
pip install numba==0.53
```


メッセージが出た
```python
Note: you may need to restart the kernel to use updated packages.
```
対処法　[参考サイトリンク](https://teratail.com/questions/230934)
カーネルのリスタート
`Restart`ボタンを押す


エラーが出た LightGBMがないよー
```python
dlopen(/Users/************): Library not loaded: */libomp/lib/libomp.dylib Referenced from: /Users/*/opt/anaconda3/lib/python3.6/site-packages/lightgbm/lib_lightgbm.so Reason: image not found
```
対処法　[参考サイトリンク](https://nshalnote.com/?p=433)
```python
brew install libomp
pip uninstall lightgbm
pip install lightgbm
```


```python
from pycaret.regression import *
```
よし！エラー解消


```python

```
