# 3.32 Flexbox 排版 - Container

Flexbox 排版模式是 CSS3 才有的東西，所有如果要使用，請留意它的支援度。來看一下 [Flexbox 的支援度](https://caniuse.com/#search=flexible)。

![Flexbox 在各瀏覽器的支援程度](../.gitbook/assets/flexbox\_support.png)



## 什麼是 Flexbox Model？

這是一個 CSS3 才出現的規範，Flexbox 引進了新的排版模式，解決元素分佈不均、空白等距無法自動均分的現象。所以透過 Flexbox 的相關樣式設定，來讓子元素自動排列。



## 如何更改某元素為 Flexbox 排版模式

```css
display: flex;
```

或

```css
display: inline-flex;
```



## 第一個 Flexbox

### 瞭解 flex 和 inline-flex

flex 會佔滿父元素的整個寬度，如同區塊元素一樣；inline-flex 則是類似行內區塊元素，與其他周圍元素會在同一行。

{% embed url="https://codepen.io/carlos411/pen/oNvdzqx" %}



### 瞭解 Flex container 和 Flex Items。

```markup
<ul>
  <li>第一項</li>
  <li>第二項</li>
  <li>第三項</li>
</ul>
```

```css
ul{
  /* 也可以是：display: inline-flex; 此為「行內 Flex」 */
  display: flex;
}
```

看看以下例子：

{% embed url="https://codepen.io/carlos411/pen/vYBmNLV" %}

發現 ul 內層的 li 變成水平排列了(且沒有空格問題)，到這邊我們需要先瞭解幾件事情：

* ul 標籤已經變成了 **Flexbox Model** 排版模式，會直接影響到其 **第一層子元素(Flex item(s))** 的排版行為。
* ul 是 Flexbox Model 中的 **Flex container**。
* li 是 Flexbox Model 中的 **Flex item(s)**，因為是 ul 的第一層子元素。
* 此範例適用於任何父層、子層元素，不僅限於 ul、li。
* Items ( 此例為 li ) 的高度，會跟著 Container ( 此例為 ul ) 的高度增加。



### 瞭解 Axis

當一個元素被設定成 `display: flex;` 或 `display: inline-flex;` 時，就會有 Main Axis(主軸) 和 Cross Axis(交錯軸)這概念：

當 `flex-direction` 是 row(預設) 或 row-reverse：

![](<../.gitbook/assets/main\_axis\_row (1).png>)

當 `flex-direction` 是 column 或 column-reverse：

![](<../.gitbook/assets/main\_axis\_column (1).png>)



## Flex Container 相關屬性，此例為 \<ul>

### flex-direction：方向如何排列

內層元素(li)沿著 **主軸(Main Axis)** 來排列，有四種方向：

* `row`：這是預設，由左至右。
* `column`：由上至下。
* `row-reverse`：row 的相反。
* `column-reverse`：column 的相反。

```css
ul{
  display: flex;
  
  /* row(default) | column | row-reverse | column-reverse */
  flex-direction: row;
}
```

{% embed url="https://codepen.io/carlos411/pen/jONmbmq" %}

### flex-wrap：是否斷行

內層元素過多的時候，該如何斷行，有三種設定值：

* `nowrap`：(預設值)，代表即使 Flex Items 數量過多，依然不會斷行，Flex Container 都會試圖去容納這些 Flex Items 在同一個軸。
* `wrap`：代表當 Flex Items 數量過多，多到 Flex Container 裝不下的時候，會斷行，斷行會延著交錯軸(Cross Axis)。
* `wrap-reverse`：代表當 Flex Items 數量過多，多到 Flex Container 裝不下的時候，會斷行，斷行會延著交錯軸(Cross Axis)的反向。

{% embed url="https://codepen.io/carlos411/pen/ExYmVEE" %}

### flex-flow：方向與斷行的縮寫

單純只是個 flex-direction 和 flex-wrap 同時用的縮寫，例如：

```css
ul{
  flex-flow: row wrap-reverse;
  
  /* 預設值是： */
  /* flex-flow: row nowrap; */
}
```

等同於：

```css
ul{
  flex-direction: row;
  flex-wrap: wrap-reverse;
}
```

### justify-content：Flex Items 如何排列

透過 `justify-content` 來設定 Flex Items 在 `Main Axis` 中該如何排列，共有六種：

* `flex-start`：這是預設值，全部置左。
* `flex-end`：全部置右。
* `center`：置中。
* `space-between`：各個 Flex Item 的空白間距相等。
* `space-evenly`：各個 Flex Item 的周圍間距相等。
* `space-around`：各個 Flex Item 的左右空白間距相等，如下圖：

![space-around 的示意圖](../.gitbook/assets/space\_around\_hint.png)

範例：

{% embed url="https://codepen.io/carlos411/pen/JjPNYVe" %}

### align-content：Flex Items 在 Cross Axis 中如何排列

透過 `align-content` 來設定 Flex Items 在 `Cross Axis(交錯軸)` 中該如何排列，共有七種。

註：因為 flex-wrap 預設是 `nowrap`，即不能斷行，所以跟本無法針對「交錯軸」來排列。所以 `align-content` 屬性若要有效，必須將 flex-wrap 的屬性值設定成 `wrap` 或 `wrap-reverse` 才會有效。

`align-content` 可以設定的值有：

* `flex-start`
* `flex-end`
* `center`
* `space-between`
* `space-evenly`
* `space-around`
* **`stretch`**：這是預設值，自動延展。(相較於 justify-content，多了這個。)

{% embed url="https://codepen.io/carlos411/pen/XWrRXKx" %}

### align-items：同排的 Flex Items 在 Cross Axis 中如何排列

透過 `align-items` 來設定沿著主軸同一排的各 Flex Items 之間，在 `Cross Axis` 中該如何排列，共有五種可以設定的值：

* `flex-start`：置頂。
* `flex-end`：置底。
* `center`：置中。
* **`stretch`**：(預設值)，自動延伸。
* `baseline`：依據 baseline 來做對齊，如下圖：

![align-items 的 baseline 對齊方式](../.gitbook/assets/align\_items\_baseline\_hint.png)

flex-direction 預設為 row：

{% embed url="https://codepen.io/carlos411/pen/BaBRjoQ" %}

將 flex-direction 改成 column 再觀察看看：

{% embed url="https://codepen.io/carlos411/pen/JjdyrMG" %}
