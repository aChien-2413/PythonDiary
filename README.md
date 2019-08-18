# PythonDiary

## 專案介紹
我的第一個網站:D

## 成品展示

[網站網址(host by heroku)](https://diary-python.herokuapp.com)
![](https://github.com/aChien-2413/PythonDiary/raw/master/chien.png)

## 使用技術

工具名稱 | 用途
---|---
Python 3 | :3
Flask(python) | 建立伺服器
HTML/CSS  | 網頁表示和排版
Heroku   | 託管網頁
GitHub   | 存放原始碼

## 程式碼片段
```python
@app.route("/")
def home():
  temp = glob.glob("articles/*")
  fill = []
  for t in temp:
    length = len(glob.glob(t + "/*.txt"))
    category = t.replace("articles/", "")
    f = (category, length)
    fill.append(f)
  print("來到首頁")
  return render_template("index.html", cat=fill)
  ```
