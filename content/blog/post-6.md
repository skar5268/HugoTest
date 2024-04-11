---
title: "Event"
date: 2021-01-22
draft: false

# post thumb
# image: "images/post/post-3.jpg"

# meta description
description: "this is meta description"

# taxonomies
categories: 
  - "JavaScript"
tags:
  - "Photos"
  - "Game"
  - "HTML"
  - "Python"
  - "New"

# post type
type: "post"
---

將內容（例如：座標、按鍵）記錄在 event 裡

```
var box;
function init(){
	//取得 id 為 "box" 物件，並且指定給 box 變數
	box = document.getElementById("box");
	
	//將 onclick 註冊給 pickup	
	box.onclick = pickup;
}
//撿起來
function pickup(){
	//設定滑鼠移動時， box 跟著移動
	document.onmousemove = move;

	//將onclick註冊給putdown所以再次按下滑鼠的時候，就是放下	
	box.onclick = putdown;
}
```
box.onclick = pickup; 這裡呼叫函式不需要()括弧？

當你在 JS 上要使用 onclick 時，不需要加上刮號，

原因是 onclick 的語法只是要對應函式位置，當下還不用執行

是等到有人觸發事件後，他自動就會執行該函式

也就是說需要馬上執行的才需要加 ()

## onclick和click差別

(1) 關於 onclick

MDN 的文件解釋：

https://developer.mozilla.org/zh-TW/docs/Web/Guide/Events/Event_handlers

on-event 處理器為透過 DOM 元素的屬性，用來協助元素如何應對事件，例如：

(a) 在元素上使用一個名稱為 on{eventtype} 的 HTML 標籤屬性（attribute）

<button onclick="return handleClick(event);">

(b) 藉由設定相對應的 JavaScript 屬性（property）

document.getElementById("mybutton").onclick = function(event) { ... } 

(2) 關於 click

MDN 的文件解釋：

https://developer.mozilla.org/zh-TW/docs/Web/API/HTMLElement/click

當 click() 被使用在 DOM 元素（像是任一 <input> 元素），便會觸發該元素的點擊事件。

事件會冒泡至 document tree（或 event chain）的上層元素，並觸發它們的點擊事件。

例如：HTMLElement.click() 方法可以模擬滑鼠點擊一個元素。

這邊做個總結：

(效果) onclick 和 click() 效果一樣。

(區別) 

onclick() 只是簡單調用按鈕 HTMLElement 的 onclick 方法，並未觸發事件。

click() 是真正地用程序去點擊按鈕，觸發按鈕的 onclick() 事件。

## 綁定事件的語法差異

onclick 不能同時綁定兩個事件

## Event Bubbling、Event Capturing 差異

```
elAdd.addEventListener('click',function(){
  alert('add-2')
},false)
```

false（事件氣泡：event Bubbling）從指定元素往外層找
true （事件捕捉：event capturing）：從最外層找到指定元素
第三個參數預設是 false

## stopPropagation - 中止冒泡事件

[DOM 的事件傳遞機制：捕獲與冒泡](https://blog.techbridge.cc/2017/07/15/javascript-event-propagation/)

## preventDefault - 取消預設觸發行為

e.preventDefault();

取消元素的默認行為

除了用在 a 連結外，也可以用在 submit 按鈕

submit 按鈕：先透過 JS 去查詢表單有無錯誤，再 post 去傳送

**post 傳送**

post 是表單傳送的方法之一，

也是 HTTP Method 的方法，

概念為「將東西傳送出去」。

往後的章節會陸續講解相關的知識。

[form表單中的get與post有什麼差別？](https://medium.com/ui-ux%E7%B7%B4%E5%8A%9F%E5%9D%8A/form%E8%A1%A8%E5%96%AE%E4%B8%AD%E7%9A%84get%E8%88%87post%E6%9C%89%E4%BB%80%E9%BA%BC%E5%B7%AE%E5%88%A5-d2a04845769a)

[宣告變數](https://ruienyuski.github.io/blog/2020/11/07/%E5%AE%A3%E5%91%8A%E8%AE%8A%E6%95%B8/)

## keyCode - 點擊鍵盤，射發火箭！

var body = document.body;
var body = document.querySelector('body');

Document 介面代表所有在瀏覽器中載入的網頁，

也是作為網頁內容 DOM Tree（包含 <body>、<table> 與其它的元素）的進入點。

Document.body 主要是「回傳目前文件的 <body> 節點，如元素不存在則回傳 null」。因此只有 body 能使用。

MDN 對 KeyboardEvent 的描述是「記錄著使用者和網頁之間透過鍵盤產生的互動事件」。

因此會是觀察整個網頁的 DOM 節點，即 document.body；。

## blur - 離開焦點時進行事件觸發

滑鼠點擊時會產生 focus 事件

離開焦點時就會觸發 blur 事件

focus：所在焦點

blur：離開焦點

## 網頁座標 - 了解 screen、page、client 箇中差異

screen：整個電腦的解析度

page：網頁的寬高(整個頁面)

client：目前瀏覽器視窗的寬高(窗口)
