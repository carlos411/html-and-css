# 2.28 影片

`<video>...</video>`

## 語意

影片

## 使用範例

controls：顯示控制列表。

autoplay：自動播放，要再加上 muted 屬性，才會自動播放。

disablePictureInPicture：關閉子母畫面。

controlsList="nodownload"：關閉下載按鈕。

poster：一開始尚未播放前的預載圖片。

loop：影片播放結束後，自動重播。

muted：靜音。

playsinline：在手持裝置(手機、平板)，想要自動可以播放影片的話，還要再加上這個屬性。

\<source>...\</source> 提供不同格式的影片，主要是讓瀏覽器從上而下依序選擇可以播放的格式，只要遇到可以播放的，就用那個來播。影片副檔名建議是 **mp4**、**ogg(或 ogv)**、**webm**。

網頁上常見的影片 `type` 類型設定：

* video/mp4
* video/ogg
* video/webm

```markup
<video width="500" controls autoplay disablePictureInPicture controlsList="nodownload" poster="https://picsum.photos/id/406/500/300" muted loop> 
  <source src="http://techslides.com/demos/sample-videos/small.mp4" type="video/mp4">
  <source src="http://techslides.com/demos/sample-videos/small.ogv" type="video/ogg"> 
</video>
```

{% embed url="https://codepen.io/carlos411/pen/gOYmbYw" %}

{% hint style="info" %}
練習：請將範例原始碼，貼至您的編輯器，實際用瀏覽器瀏覽，並改變各種參數試試。
{% endhint %}
