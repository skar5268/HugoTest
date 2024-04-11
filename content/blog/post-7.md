---
title: "localStorage - 瀏覽器資料儲存"
date: 2021-01-25
draft: false

# post thumb
# image: "images/post/post-4.jpg"

# meta description
description: "this is meta description"

# taxonomies
categories: 
  - "localStorage"
tags:
  - "Photos"
  - "Game"
  - "HTML"
  - "Python"
  - "New"

# post type
type: "post"
---

## 什麼是 localStorage ？

瀏覽器的資料庫

**localStorage儲存資料型態**

HTML 5 新增 localStorage 特性，主要是解決 cookie 儲存空間不足的問題( cookie 中每條 cookie 的儲存空間為 4k )，

所以他只能存字串，再用 JSON.parse 轉為陣列讓  JS 去使用裡面的資料，所以裡面就算寫入數字、布林值等..

他還是會轉成字串儲存在瀏覽器，如同下面這篇文章內文中 localStorage 的侷限第四點

https://codertw.com/%E5%89%8D%E7%AB%AF%E9%96%8B%E7%99%BC/232745/

「 localStorage 本質上是對字串的讀取，如果儲存內容多的話會消耗記憶體空間，會導致頁面變卡」

## setItem、getItem 基本操作

設定一個內容
```
localStorage.setItem("myname",str);
```

取出 item 的內容

```
console.log(localStorage.getItem('myname'));
```

[setItem、getItem 基本操作
](https://codepen.io/skar5268/pen/wvzLaxE?editors=1010)

## 透過 JSON.parse、JSON.stringify 來編譯資料

因為 localStorage 只會保存 string 資料，如果要讀取陣列的資料需要使用 JSON：

1. 先將 array 轉成 string
```
JSON.stringify()
```
2. 要讀取資料時，將 string 轉成 array
```
JSON.parse()
```

[透過 JSON.parse、JSON.stringify 來編譯資料
](https://codepen.io/skar5268/pen/VwKJvwy?editors=1011)

## data-* - 透過 dataset 讀取自訂資料

```
document.querySelector('.list li').dataset;
document.querySelector('.list li').dataset.dog;
```

[data-* - 透過 dataset 讀取自訂資料
](https://codepen.io/skar5268/pen/ZEpdbyp)

## dataset、array 運用

[dataset、array 運用](https://codepen.io/skar5268/pen/ZEpdKmz?editors=0011)

## splice - 刪除 array 資料
