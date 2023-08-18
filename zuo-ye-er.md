# 5 作業：網頁切版

## 作業內容

完成以下兩張圖片的切版。

1、商品列表頁

<figure><img src=".gitbook/assets/固定式版型_商品列表頁.png" alt=""><figcaption></figcaption></figure>

2、商品詳細頁



<figure><img src=".gitbook/assets/固定式版型_商品詳細頁.png" alt=""><figcaption></figcaption></figure>



說明：

1、完成上面兩張圖的網頁切版，固定式版型 1200px，在頁面置中。

2、在 html\_css 資料夾裡建立一個資料夾，叫 **`assignment`** 資料夾。

3、在 assignment 資料夾裡，建立 **`images`** 資料夾，[下載圖檔](https://alldata.sgp1.digitaloceanspaces.com/sample/html\_css\_images.zip)，將圖檔放到 images 資料夾裡。

4、在 assignment 資料夾裡，建立 **`shop_list.html`** 及 **`shop_detail.html`** 兩個網頁檔。

5、在 assignment 資料夾裡，建立 **`css`** 資料夾。



## 各步驟

### 步驟一：header 區域

在兩個頁面，body 標籤裡面，放以下的結構，留意 **`-on`**：

```html
<header class="header">

  <div class="block">

    <nav class="nav">
      <a href="./shop_list.html" class="logo"><img src="./images/logo.png"></a>

      <ul class="nav_list">
        <li><a href="./shop_list.html" class="-on">花禮種類</a></li>
        <li><a href="./shop_detail.html">花產品介紹</a></li>
      </ul>

      <div class="share_block">
        <span class="share_text">社群連結</span>
        <ul class="share_list">
          <li><a href="https://www.facebook.com">FB 粉絲頁</a></li>
          <li><a href="https://instagram.com">IG 頁面</a></li>
        </ul>
      </div>

    </nav>

  </div>

</header>
```





## 繳交方式

於以下網址繳交：

[https://frontend.tibame.com](https://frontend.tibame.com)

將 **`assignment 資料夾`**壓縮變成壓縮檔(zip 檔或 rar 檔)，繳交該壓縮檔即可。



## 繳交期限

繳交期限 /() 晚上 12 點之前。



## 參考作法

