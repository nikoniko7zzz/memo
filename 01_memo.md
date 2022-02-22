- [環境設定](#環境設定)
- [requirements.txtに書き込む](#requirementstxtに書き込む)
- [対話モード](#対話モード)
- [vscode リロード](#vscode-リロード)
- [環境変数(APIキーなど、Githubに出せないものを変数で呼び出す)](#環境変数apiキーなどgithubに出せないものを変数で呼び出す)
- [Github](#github)

# 環境設定
このpythonフォルダの中は、一つの仮想空間で管理する
(environment_3_9_7) niko@kunikonoMacBook-Pro python % which python3
/Users/niko/Desktop/MyApp/study/python/environment_3_9_7/bin/python3

- 入る
`source environment_3_9_7/bin/activate`
- 出る
`deactivate`
___

# requirements.txtに書き込む
`pip freeze > requirements.txt`
___
# 対話モード
- 入る
`python`
- 出る- [環境設定](#環境設定)
`contrl` + `z`
___

# vscode リロード
command+shift+p -> reload


# 環境変数(APIキーなど、Githubに出せないものを変数で呼び出す)

- インストール
```python
pip install python-dotenv
```
- 環境変数として呼び出すファイル
```python
# .env ファイルをロードして環境変数へ反映
from dotenv import load_dotenv
import os
load_dotenv()
openai.api_key = os.getenv("OPENAI_API_KEY")
```
- .envファイル
```python
OPENAI_API_KEY=***********************
```

- .envファイルはGithubにはあげたくないので
  .gitignoreファイルに明示する
```python
.env
```

# Github
```python
git push -f
git push origin master -f
```