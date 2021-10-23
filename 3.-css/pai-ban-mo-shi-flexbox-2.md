# 3.33 Flexbox 排版 - Items

## Flex Item(s) 相關屬性，此例為 \<li>

請留意 flex-direction 預設值是 row，代表 Main Axis(主軸)是橫向，以下範例都是以 `flex-direction: row` 來設定，之後同學可試著將 flex-direction 改成 column (也就是將 Main Axis 改成直向)觀察看看。

共有六種屬性可以設定，以下解說：

### order：指定順序

order 可以是任何的整數，所有的 Flex Items 預設值都是 0。然而所有的 Flex Items 的排列順序都會按照 order 值的大小來針對 Main Axis (主軸)排列，從最小開始排，依序排到最大值。

{% embed url="https://codepen.io/carlos411/pen/wvwqBjz" %}



### flex-grow：有多餘空間時，如何分配剩餘空間

設定讓該 Flex Item 會自行針對 Main Axis 延展，將多餘空間給佔滿。然而 flex-grow 預設值都是 0，其實就是代表將此功能關閉。設定大於等於 1 的整數，就會按比例自動填滿剩餘空間。

例 1：只設定其中一個 flex-grow

{% embed url="https://codepen.io/carlos411/pen/MWgvwgX" %}

例2：設定有多個 flex-grow 大於等於 1 時，「**剩餘空間**」自動依比例分配。

{% embed url="https://codepen.io/carlos411/pen/KKPvwEZ" %}



### flex-shrink：Flex Container 空間不夠時，如何壓縮 Flex Items

預設值是1，也就是當空間超出 flex container 的寬度時，每一個 flex items 都會被平均壓縮。

例：\
設定 Flex Container 的寬度為 800px；\
共5個 Flex Items ，設定寬度為 200px。\
多出 1000 - 800 = 200。\
則每個 Flex Item 平均被壓縮40px，最後的寬度會是 160px。才不會超出 Flex Container 的寬度。

{% embed url="https://codepen.io/carlos411/pen/PoYKqwW" %}



### flex-basis：設定 Flex Item 的寬度或高度

設定 flex-basis 是沿著 **Main Axis(主軸)** 來設定 Flex Items 的寬或高。

* 當 flex-direction 為 `row` 或 `row-reverse` 時，設定 flex-basis 等同於設定寬度(width)。
* 當 flex-direction 為 `column` 或 `column-reverse` 時，設定 flex-basis 等同於設定高度(height)。
* flex-basis 的優先權會高於 width 和 height。
* flex-basis 的預設值是 auto。



範例1：設定寬度：

{% embed url="https://codepen.io/carlos411/pen/XWrabxr" %}



範例2：設定高度：

{% embed url="https://codepen.io/carlos411/pen/eYOrWmY" %}



### flex：縮寫形式

預設值：

```css
flex-grow: 0;
flex-shrink: 1;
flex-basis: auto;
```

等同於

```css
flex: 0 1 auto;
```

也就是 flex 是 flex-grow、flex-shrink、flex-basis 的縮寫。



### align-self：只設定自己在這排的對齊位置

與 Flex Container 的 `align-items` 的觀念一模一樣。差別在於這是設定自己這個 Flex Item。

可以設定的值有：

* `auto`：(預設值)，表示與 Container 所設定的 `align-items` 值一樣。
* `flex-start`
* `flex-end`
* `center`
* `baseline`
* `stretch`

{% embed url="https://codepen.io/carlos411/pen/yLBoVyj" %}



## 練習

### 一、水平垂直方向的置中

提供 html：

```markup
<div class="outer">
  <div class="inner">這是內容<br>這是第二行內容</div>
</div>
```

請撰寫 css，結果如下圖：

![](../.gitbook/assets/flexbox\_center\_block.png)

也就是將藍框的部份，置於黑框的中間。



參考作法：

{% embed url="https://codepen.io/carlos411/pen/QWbOOjZ" %}



### 二、使用 flexbox 做固定式二欄排版

提供 html：

```markup
<div class="outer_block">
  <div class="left_block">左欄<br>第二行</div>
  <div class="right_block">右欄</div>
</div>
```

請撰寫 css，結果如下圖：

![](../.gitbook/assets/flexbox\_two\_columns.png)



參考作法：

{% embed url="https://codepen.io/carlos411/pen/mdJxoXP" %}



## 參考資源

[CSS Flexbox](https://www.w3schools.com/css/css3\_flexbox.asp)
