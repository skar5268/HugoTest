---
title: "JavaScript"
date: 2021-01-19
draft: false

# post thumb
# image: "images/post/post-2.jpg"

# meta description
description: "this is meta description"

# taxonomies
categories: 
  - "JavaScript"
tags:
  - "Photos"
  - "HTML"
  - "Python"
  - "New"

# post type
type: "post"
---

## 變數

### 變數簡介



#### 變數常見資料型別

* 數字、字串、布林（true、false）
* 變數裡面是空的，沒有任何值，預設就會是 undefined
* 撈文字裡面的內容 用 value
* typeof 查詢字串還是數字還是函式等
* parseInt


## 函式

### 定義

函數：是一個任務會幫你執行裡面的算式

函式寫法：**宣告函式 函式名稱**

```
function greet(){

alert('歡迎光臨！');

alert('請問你要點些什麼？')

}
```

**執行函數**

greet(); *呼叫它後才會執行裡面的內容*

函式名稱後面要括號()

之前講到變數 有提到 var box = 10 會出現undefined的原因

var box;

box = 10

分成兩步驟

### 問答區


**1. 為什麼執行函式的下一行會出現 undefined？**

該值表示回傳的結果～

在 Chrome Devtool 執行一個命令都類似執行一個函式，

而這個函式由於沒有 return 任何值，所以會回傳 undefined

程式碼載入 JavaScript 以後

他會自動把 function 放在最上面執行，也就是優先處理 function

所以你不管放在哪裡的話

function 都會放在最上面去做執行

**2. JavaScript裡的語句用分號結尾是個選項嗎**

建議在寫程式碼最後結尾養成寫分號的習慣

主要是分號是代表語句分隔的意思

最常見的是在用 var 宣告變數後加上分號

如 var a = 1;

如果沒加上分號，下方程式碼會不了解後方的 kk 是否為 str 的內容

`> var str = {'name': 'tom'} var kk = 3;`

詳細可參考[這篇文章](https://eddychang.me/js-semicolon/)

宣告在函數裡的變數，只存在於函數裡

**函式帶參數**

function count(oneNum){

var total = oneNum *10;

console.log('總數等於：' + total);

}

count(10)

運算到小數點的方法：

小數點可以使用 toFixed 讓它顯示後面幾位的內容

document.getElementById('totalId').textContent = total.toFixed(2); // 112.47

參數其實就是我們會帶入 function 的變數，在呼叫時候，把裡面的值傳遞到 function 裡面去執行，與一般變數不同，不用 var 去宣告他

function 有 hoisting 觀念，它會自動把 function 放在最上面

在JavaScript中undefined和not defined是不一樣的，undefined其實是一個值，not defined則是沒有定義過這個變項。

https://pjchender.blogspot.com/2015/12/javascript-hoisting.html

如果在 `var` 的變數前加入 `console.log()`，這個時候並不會出錯，則是會跳出 `undefined`，這表示這個變數在記憶體中已經有一個位置，只不過目前並沒有值。

https://wcc723.github.io/javascript/2017/12/16/javascript-hoisting/

JavaScript 是屬於單執行緒的程式語言  
程式碼遇錯後則會中斷不再繼續執行  
j若遇到未被定義的變數，則此錯誤造成後續程式碼不再執行
