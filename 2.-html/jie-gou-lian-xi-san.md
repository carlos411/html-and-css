# 2.33 作業一

## 建立一個網頁，檔名 form.html，建立如下表單：

請在 `html_css` 資料夾下，建立 `assignment1` 資料夾，再建立 `form.html` 檔案。

注意事項：

* form 標籤的 action 屬性，設定成 `http://notes.webmix.cc/ex.php`。method 屬性，設定成 `get`。
* 帳號 `name="username"`；密碼 `name="password"`；飲食 `name="food_type"`，「葷」 這個的 value 請設定成「葷」；「素」 這個的 value 請設定成「素」。
* 密碼欄位，type 設定成 `password`。
* 人數 `name="num"` 的下拉選單，建立「1位」、「2位」、「3位」。分別 option 的value 為 1、2、3。
* 興趣：input 的 `type="checkbox"`，`name="habits[]"`，value 分別是 **`運動`**、**`旅遊`**、**`電影`**。
* 其它事項 `name="notes"`。
* 飲食 radio button 及興趣 checkbox，請優化點擊範圍，點擊文字，也要能選得到。
* 資料送出的按鈕，type 設定成 `submit`。

完成示意圖：

![基本 form 表單](../.gitbook/assets/habits\_form.png)

假設輸入以下資料，點擊「資料送出」按鈕後：

![假設輸入表單資料](../.gitbook/assets/send.png)

結果應如下圖(觀察網址)：

![](<../.gitbook/assets/send\_result (1).png>)

參考作法：

[https://alldata.sgp1.digitaloceanspaces.com/sample/html\_css\_assignment1.zip](https://alldata.sgp1.digitaloceanspaces.com/sample/html\_css\_assignment1.zip)

## 作業繳交

### 方式：Tibame 平台 (TFD104 優先使用)

[http://frontend.tibame.com/](http://frontend.tibame.com)

只需繳交 form.html 檔案即可。

繳交期限：9/29(三)

## 觀察 post 資料傳遞

form 標籤的 action 屬性，請改成 `http://notes.webmix.cc/ex_post.php`。method 屬性，設定成 `post`。





form.html：

```html
<!DOCTYPE html>
<html lang="zh-Hant">
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>

    <form action="https://notes.webmix.cc/ex.php" method="get">

      <div>
        <label for="username">帳號：</label>
        <input type="text" id="username" name="username">
      </div>

      <div>
        <label for="password">密碼：</label>
        <input type="password" id="password" name="password">
      </div>

      <div>
        <label>飲食：</label>
        <input type="radio" name="food_type" value="葷" id="type1" checked> <label for="type1">葷</label>
        <input type="radio" name="food_type" value="素" id="type2"> <label for="type2">素</label>
      </div>

      <div>
        <label>人數：</label>
        <select name="num">
          <option value="1">1位</option>
          <option value="2">2位</option>
          <option value="3">3位</option>
        </select>
      </div>

      <div>
        <label>興趣：</label>
        <input type="checkbox" name="habits[]" value="運動" id="habit1"><label for="habit1">運動</label>
        <input type="checkbox" name="habits[]" value="電影" id="habit2"><label for="habit2">電影</label>
        <input type="checkbox" name="habits[]" value="旅遊" id="habit3"><label for="habit3">旅遊</label>
      </div>

      <div>
        <label>其它事項：</label><br>
        <textarea rows="10" cols="30" name="notes"></textarea>
      </div>

      <div>
        <button type="submit">資料送出</button>
      </div>
    </form>


  </body>
</html>
```

