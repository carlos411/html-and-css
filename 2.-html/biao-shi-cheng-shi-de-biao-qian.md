# 2.4 表示程式的標籤

`<code>...</code>`

## 語意

如果想表示這是**一段程式**，就可以用 `<code>` 標籤；然後是多行的程式碼的話，也會與 `<pre>` 標籤搭配使用，因為可以保留縮排、空格這樣的文字。

## 範例

```markup
<code>echo</code>

<pre><code>
function(){
  alert("this is function");
}
</code></pre>
```

{% embed url="https://codepen.io/carlos411/pen/VwZPozj" %}

{% hint style="info" %}
練習：請將範例的原始碼，貼至您自己的編輯器，並用瀏覽器觀察。
{% endhint %}

