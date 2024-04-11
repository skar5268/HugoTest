---
title: "DOM"
date: 2021-01-19
draft: false

# post thumb
# image: "images/featured-post/post-3.jpg"

# meta description
description: "this is meta description"

# taxonomies
categories: 
  - "JS"
tags:
  - "Photos"
  - "Game"
  - "React"
  - "Python"
  - "New"

# post type
type: "post"
---


https://ithelp.ithome.com.tw/articles/10202689

querySelector 與 getElementById 的差異
(1) 相同點：選取 HTML 元素

(2) 相異點

(a) document.getElementById()：選取元素侷限於 id 元素，在網頁上 id 不能重複，只會有唯一一個。

例如：var msg = document.getElementById(‘hi’);

(b) document.querySelector()：選取元素包含 html標籤、id 元素、class 元素。

例如：var msg = document.querySelector(#hi);

若對 兩者的差異 想要更進一步了解，附上相關網址供你參考：https://ithelp.ithome.com.tw/articles/10211605

插入 HTML 標籤的兩種方法

![](https://i.imgur.com/bzJdmdy.png)

![](https://i.imgur.com/cwty8ym.png)



在 HTML 世界哩，用的每一個網頁結構都算是一個節點

textContent 只是單純去新增文字的節點
innerHTML 增加 HTML 標籤在裡面。他會先將裡面**全部清空**，再賦予值進去

 querySelectorAll 是為多項目設計的，因此使用時必須搭配for迴圈才能將值帶入
 
 這邊補充說明 document.querySelector() 和 document.querySelectorAll() 的差異性：

(a) 關於 document.querySelector()

document.querySelector() 只會回傳 document 選到的第一個 class 元素，

因此搭配 innerHTML 的寫法如下：

```
// HTML 部份
<ul class='list'>
 <li> 我是第一個 li 標籤 </li>
 <li> 我是第二個 li 標籤 </li>
</ul>

// JS 部份
var list = document.querySelector('.list li');
list.innerHTML = '<li>被替換了</li>';
```


(b) 關於 document.querySelectorAll()

假如是選取 'list' class 名稱內所有的 li 元素，

搭配 innerHTML 的寫法如下：
```

// JS 部份
// 選取 'list' class 名稱內所有的 li 元素
var list = document.querySelectorAll('.list li');

// 替換 'list' class 名稱內所有的 li 元素的內容
for (var i = 0; i < list.length; i++) {
 list[i].innerHTML = '<li>被替換了</li>';
}
```

[JavaScript String (字串)
](https://www.fooish.com/javascript/string/)


createElement 新增元素
appendChild 增加子節點，會動態加在後面(跟 innerHTML 不同)

innerHTML 有資安疑慮，如果取得的資料是由使用者填寫送出的，則有可能被塞惡意程式。因此若要使用 innerHTML，需要用可以信任的資料來去渲染出來。
**表單輸入盡量不要用 innerHTML**
