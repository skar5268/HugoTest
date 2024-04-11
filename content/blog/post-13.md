---
title: "指令語法全介紹｜操作畫面超容易"
date: 2021-04-30
draft: false

# post thumb
# image: "images/post/post-3.jpg"

# meta description
description: "this is meta description"

# taxonomies
categories: 
  - "Vue"
tags:
  - "Photos"
  - "Game"
  - "HTML"
  - "Python"
  - "New"

# post type
type: "post"
---
# 指令語法全介紹｜操作畫面超容易

## 指令觀念介紹
![](https://i.imgur.com/TFpUsC9.png)

![](https://i.imgur.com/BjNfQi1.png)

### 專有名詞
**1. 指令 - Directives：**
![](https://i.imgur.com/PD5rdXW.png)

**2. 修飾符 - Modifiers：**
修飾符可以讓 v-model 更好運作
![](https://i.imgur.com/eT1XP3E.png)

**3. 縮寫 - Shorthands：**
![](https://i.imgur.com/fqCuvHF.png)

## 綁定內容於畫面上 v-text

v-text、{{}} (Mustache) 純文字的渲染
雙向綁定的特色：在操作資料的時候，畫面也會跟著變化

v-htm：渲染到畫面上的時候依然保有 HTML 的特色、使用這個方法需要確保資料是安全的
[注意事項](https://vue3js.cn/docs/zh/api/directives.html#v-html)

v-once 單次綁定，後面不需要加參數

v-pre 讓文字不會被轉譯，可以顯示 {{}}


## 多筆資料渲染 v-for

## 條件判斷 v-if
判斷 HTML 的節點是否呈現
v-show 只是把節點隱藏，v-if 則是把節點刪除

## HTML 屬性綁定 v-bind
v-bind:綁定的屬性 = "值"
簡化 >> :綁定的屬性 = "值"

## HTML 樣式綁定

## 資料雙向綁定 v-model

### v-model 與表單

### v-model 修飾符
v-model.lazy（HTML 的 change 事件）
v-model.number（將輸入的文字轉為 number 型別）
v-model.trim（移除使用者輸入的前後空白）


### 事件觸發 v-on
![](https://i.imgur.com/oFO1XE1.png)

v-on 通常不太會直接跟 data 產生關係，大部分會直接來觸發 methods，透過這個 methods 來做更多事情

### v-on 修飾符

### v-on DOM 事件處理技巧
