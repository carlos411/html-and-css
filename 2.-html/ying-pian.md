# 2.28 影片

`<video>...</video>`

## 語意

影片

## 使用範例

controls：顯示控制列表。

autoplay：自動播放，實測的結果有的瀏覽器不會自動播放。

disablePictureInPicture：關閉子母畫面。

controlsList="nodownload"：關閉下載按鈕。

poster：一開始尚未播放前的預載圖片。

loop：影片播放結束後，自動重播。

muted：靜音。

playsinline：針對 iOS ，在播放影片的時候，可以不用自動全螢幕。\(參考： [New  Policies for iOS](https://webkit.org/blog/6784/new-video-policies-for-ios/)\)

&lt;source&gt;...&lt;/source&gt; 提供不同格式的影片，主要是讓瀏覽器從上而下依序選擇可以播放的格式，一般建議主要是 **mp4**、**ogg\(或 ogv\)**、**webm**。

網頁上常見的影片 `type` 類型設定：

* video/mp4
* video/ogg
* video/webm

```markup
<video width="500" controls autoplay disablePictureInPicture controlsList="nodownload" poster="https://picsum.photos/id/406/500/300" loop> 
  <source src="http://techslides.com/demos/sample-videos/small.mp4" type="video/mp4">
  <source src="http://techslides.com/demos/sample-videos/small.ogv" type="video/ogg"> 
  出現這個訊息，表示您的瀏覽器不支援 HTML5 video 標籤。
</video>
```

{% embed url="https://codepen.io/carlos411/pen/gOYmbYw" %}

{% hint style="info" %}
練習：請將範例原始碼，貼至您的編輯器，實際用瀏覽器瀏覽，並改變各種參數試試。
{% endhint %}



