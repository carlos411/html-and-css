# 2.29 音訊

`<audio>...</audio>`

## 語意

用來播放音訊檔。

## 使用範例

controls：顯示控制列

loop：自動重播

&lt;source&gt;...&lt;/source&gt; 提供不同格式的聲音檔，主要是讓瀏覽器從上而下依序選擇可以播放的格式，一般建議主要是 **mp3**、**ogg\(或 ogv\)**。

網頁上常見的音訊 `type` 類型設定：

* audio/mpeg
* audio/ogg

```markup
<audio controls loop>
  <source src="https://www.w3schools.com/jsref/horse.mp3" type="audio/mpeg">
  <source src="https://www.w3schools.com/jsref/horse.ogg" type="audio/ogg">
  出現這個訊息，表示您的瀏覽器不支援 HTML5 audio 標籤。
</audio>
```

{% embed url="https://codepen.io/carlos411/pen/mdbWyEO" %}



