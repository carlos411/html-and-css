# 2.26 音訊

`<audio>...</audio>`

## 語意

用來播放音訊檔。

## 使用範例

屬性的部份：

controls：顯示控制列。

autoplay：自動播放。

controlsList="nodownload"：關閉下載按鈕。

loop：自動重播。

muted：靜音。



\<source>...\</source> 提供不同格式的聲音檔，主要是讓瀏覽器從上而下依序選擇可以播放的格式，一般建議主要是 **mp3**、**ogg(或 ogv)**。

網頁上常見的音訊 `type` 類型設定：

* audio/mpeg
* audio/ogg

```markup
<audio controls loop>
  <source src="https://www.w3schools.com/jsref/horse.mp3" type="audio/mpeg">
  <source src="https://www.w3schools.com/jsref/horse.ogg" type="audio/ogg">
</audio>
```

{% embed url="https://codepen.io/carlos411/pen/mdbWyEO" %}
