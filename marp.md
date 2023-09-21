---
marp: true
title: Marp
paginate: true
theme: uncover
---


### Markdown Marp VSCode 套件使用教學

---

## 目錄

---

<style scoped>
  ol {
    font-size:34px
  }
</style>
1. [介紹](#介紹)
2. [什麼是Markdown](#什麼是Markdown)
3. [安裝](#安裝)
4. [基本設定](#基本設定)
5. [基本語法](#基本語法)
6. [導出投影片](#導出投影片)
7. [常見問題](#常見問題)
8. [總結](#總結)
9. [參考資源](#目錄參考資源)

--- 

# 介紹

---

`Marp` 是一個基於 Markdown 語法的投影片製作工具。

可以使用 Markdown 語法 快速建立 報告用的投影片

---

## 什麼是Markdown 

> Markdown是一種輕量級標記式語言，它允許人們使用易讀易寫的純文字格式編寫文件，然後轉換成有效的XHTML文件。

[來源](https://zh.wikipedia.org/zh-tw/Markdown)

---

# 安裝

---

有 VsCode 專用套件和 獨立的 CLI 可以做選擇

![width:800px](/image/photo_2023-09-15_17-48-34.jpg)

---

`本次以 VsCode 套件為主`

安裝 Marp 非常簡單
只要在 VsCode 中安裝[Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)的 Plugin 即可。

---

# 基本設定

---


要在 VsCode 使用 Marp ，
首先我們要在文件最上方加入以下內容：

```
--- 
marp: true 
theme: gaia
paginate: true
---
```


---

告訴Vscode 我們開始使用 marp的套件了

```java
marp : boolean
```

---

theme 是指簡報主題的意思，
Marp 預設提供了 3 種簡報主題：
<br>

- Default 預設主題
- uncover 主題具有三個設計理念：簡約、簡約、現代
- Gaia 主題基於[yhatt/marp](https://github.com/yhatt/marp)的經典設計

<br>

每種主題在背景顏色，
Markdown文字的擺放位置都會有差異

[參考說明](https://github.com/marp-team/marp-core/tree/main/themes?source=post_page-----eab8a0668733--------------------------------#readme)

---

paginate 為 顯示頁數的選項

```java
paginate:boolean
```

---

# 基本語法

---

1. 分頁

可使用 `---` 標記來分隔不同頁面的 Slide
```markdown
# Page 1
Hello World!

---

# Page 2
magic word
```

---

2. 設定圖片寬度

```markdown
![width:200px](image_path.jpg) <!-- 設定圖片寬度為 200px -->
![height:300px](image_path.jpg) <!-- 設定圖片高度為 300px -->
![width:200px height:300px](image_path.jpg) <!-- 同時設定兩者屬性 -->
![w:32 h:32](image_path.jpg) <!-- 設定圖片大小為 32x32 px -->
![width:90% height:80%](image_path.jpg) <!-- 設定圖片大小為 90% 寬度 x 80% 高度  -->
```

---

3. 設定圖片特效

```markdown
![blur](image_path.jpg) <!-- 圖片 模糊化  -->
![blur:10px](image_path.jpg) <!-- 圖片模糊化，參數為 10px(越大越模糊)  -->
![grayscale:1](image_path.jpg) <!-- 圖片灰階化  -->
![brightness:.8 sepia:50%](image_path.jpg) <!-- 多重特效設定 -->
```