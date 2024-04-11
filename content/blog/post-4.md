---
title: "控制判斷"
date: 2021-01-19
draft: false

# post thumb
# image: "images/post/post-1.jpg"

# meta description
description: "this is meta description"

# taxonomies
categories: 
  - "JS"
tags:
  - "Photos"
  - "Game"
  - "HTML"
  - "Python"
  - "New"

# post type
type: "post"
---

#### 一、比較運算子

等於：`== 會自動幫你轉型 ex.1 == '1' 為 true` `===為嚴謹模式`

不等於：!==

布林：true false

*一個等於，是賦予值的意思，而兩個等於則是內容進行比較*

Javascript 進階 3-7 寬鬆相等、嚴格相等以及隱含轉型

https://ithelp.ithome.com.tw/articles/10229398

運算子 == 的資料格式轉換 (type conversion) 問題

規則說明：

https://es5.github.io/#x11.9.3

#### 二、邏輯運算值

And：&&

OR：||

NOT：!

if - 簡報介紹

![](https://i.imgur.com/SHIRbZp.jpg)


switch - 簡報介紹

![](https://i.imgur.com/s1MJqde.jpg)


if 在瀏覽器編譯時，會全部看過一次，所以在編譯的速度和效能上比較不好

switch 只會看哪一個 case 符合，在去跑裡面的程式碼，但 switch 最好裡面有很多條件時再使用

「當是一個範圍的時候, ex 介於某區間 大於小於多少 --->用 if else」

「當是一個特定的明確 case 做比對時 --->用 switch 」

if/else if ：會審視所有條件，若有符合條件才會執行大括號裡面的內容。
switch ：不會審視所有條件是否符合，而是會根據一開始所給的變數狀態，直接跳到符合條件那行，再去執行程式內容。
