---
title: "元件"
date: 2021-05-07
draft: false

# meta description
description: "this is meta description"

# type
type: "post"
---

## 元件介紹

### 為什麼要拆解成元件
1. 增加程式碼的可複用性
2. 避免單一檔案過大
3. 易於管理及協作
4. 元件功能獨立化

### 頁面元件結構
![](https://i.imgur.com/SpYxIIm.png)

### 元件資料獨立與傳遞
![](https://i.imgur.com/MPkxUED.png)

資料傳遞方向：

![](https://i.imgur.com/1iLpUzy.png)

props 把資料由外層轉向內層



元件：
內層所有的 data 都必須用 function return
