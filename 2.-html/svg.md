# 2.26 SVG

簡單介紹，主要是先讓同學瞭解有 SVG 這種格式圖片，未來有需要可再深入研究。

## 簡介

繪製幾何圖形、圖表，使用 svg 所繪製出來的圖，因為是屬向量格式，所以並不會因為放大之後，產生模糊的現象。

## 範例 1：畫直線

```markup
<svg>
  <line x1="5" y1="5" x2="50" y2="50" stroke="#abcdef">
</svg>
```

{% embed url="https://codepen.io/carlos411/pen/XGWZqV" %}
svg line
{% endembed %}



## 範例 2：畫圓形元素

```markup
<svg>
  <circle cx="50" cy="50" r="50" fill="#abcdef">
</svg>
```

{% embed url="https://codepen.io/carlos411/pen/ErGBGG" %}
svg circle
{% endembed %}

{% hint style="info" %}
練習玩玩看範例的 svg
{% endhint %}
