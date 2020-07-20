# 3.2 作業二說明，共用 CSS

## 作業二說明

在 html\_css 資料夾下，建立下圖 **assignment2** 資料夾裡的相關檔案：

![](../.gitbook/assets/assignment2_dir%20%281%29.png)

建完之後，即有以下檔案：

* assignment2/css/common/header.css
* assignment2/css/contact.css
* assignment2/css/index.css
* assignment2/contact.html
* assignment2/index.html

### 各檔案內容

index.html：

```markup
<!DOCTYPE html>
<html lang="zh-Hant">
  <head>
    <meta charset="utf-8">
    <title></title>
    <link rel="stylesheet" href="./css/index.css">
  </head>
  <body>
    <header>
      <p class="para1">這是 header 裡的段落</p>
    </header>

    <a href="./contact.html">連到 contact.html</a>
  </body>
</html>

```

contact.html：

```markup
<!DOCTYPE html>
<html lang="zh-Hant">
  <head>
    <meta charset="utf-8">
    <title></title>
    <link rel="stylesheet" href="./css/contact.css">
  </head>
  <body>
    <header>
      <p class="para1">這是 header 裡的段落</p>
    </header>

    <a href="./index.html">連到 index.html</a>
  </body>
</html>

```

./css/index.css

```css
@import "./common/header.css";

a{
  color: blue;
}
```

./css/contact.css

```css
@import "./common/header.css";

a{
  color: red;
}

```

./css/common/header.css

```css
header{
  border: 1px solid red;
}

```

