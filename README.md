## 考題說明
* 花30分鐘準備關於rel=noopener的報告，來跟完全沒有技術背景的人解釋說為什麼網站的對外連結最好要加上這個參數
* 就你的認知用AngularJS, Angular, React, Vue 這些前端框架跟用 jQuery 相比之下的好處是什麼？壞處又是什麼？
* 你認為寫網頁/前端開發的時候有什麼注意的事情？
* 請說明HTML/CSS/Javascript分別在前端扮演什麼角色/有什麼用?

## 主題：rel="noopener"
## 目的：為什麼網站的對外連結最好要加上這個參數

* 有一個對外的連結，我會這樣寫 html 語法。
* 意思是會新開一個視窗來連結這個網頁
```html 
<a href="http://example.com" target="_blank">連結</a>
```
### 那「沒加rel=noopener」和「有加rel=noopener」的差別在哪裡？

* Demo網站：http://keenwon.com/demo/201603/noopener.html

* 沒加rel="noopener"
* http://keenwon.com/demo/201603/noopener2.html
```html 
<a href="http://keenwon.com/demo/201603/noopener2.html" target="_blank">没有rel=noopener</a>
```

* 有加rel="noopener"
* http://keenwon.com/demo/201603/noopener2.html
```html
<a href="http://keenwon.com/demo/201603/noopener2.html" target="_blank" rel="noopener">有rel=noopener</a>
```

### 說明
* Demo 網頁有 2 個連結
* 第一個是沒有加上 rel=noopener 的 target=”_blank” 對外連結。
* 第 2 個連結，是有加上rel=noopener的target="_blank" 對外連結，點取之後，2 個連結的變化是不同的。
* 你會發現第 1 個連結點取後，原生網頁被換掉了，被換成「百度」首頁。
* 第 2 個連結點取後，原生網頁還是存在的。如果第 1 個連結頁 (DEMO) 跳轉到釣魚網站呢?

### 實際情境
* 你在一個電商網站刷卡購物，點取一個連外連結，原本的電商網站跳轉後，直接提示用戶登入，而此時你注意力集中在新開的視窗頁面裡，以為原來的電商網站帳號被登出了，你會又在登入一次繼續購物，很可能不會注意到原來的電商網頁在後台的變化，這時你的登入帳號和密碼，已經被釣魚網站給取走了。

### 教學影片
* target="_blank" vulnerability example using Facebook
* https://www.youtube.com/watch?v=ITC2RBCqUb8