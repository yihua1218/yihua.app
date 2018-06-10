# [yihua.app](https://yihua.app/)

The personal application for my daily life.

## 想做的功能

### 各種儀表板

1. 社群平台: Facebook, Twitter, Plurk, Google+...
2. 電子郵件帳號: GMail, Outlook...
3. 群組平台: Slack, Microsoft Temas...
4. Task: To Do List, GitHub, GitLab...
5. 財務: 電子發票、電子帳單、帳戶...
6. 投票: 投票或意見調查
7. 書籤、短址： goo.gl

## Vote System

1. 訂定投票事件: 開始與截止日期、事件名稱、事件說明
2. 事件投票選項: 
3. 票數限制: 每一個 IP 每日一票，單選、複選或多選(一人三票之類的)
4. 首頁： 今日事件，歷史事件回顧查詢
5. Dashboard: 當下議題與事件、每小時投票數量、在線人數、熱門查詢項目...

### 資料表設計

1. 使用何種資料模型
2. 資料關聯
3. 投票限制設計

## Firebase

### Authentication

[Using Firebase Authentication With Nuxt.js](https://www.davidroyer.me/blog/using-firebase-authentication-with-nuxtjs), [DavidRoyer](https://www.davidroyer.me/)

## Project Initialization

``` bash
$ nvm use stable
$ vue init nuxt-community/pwa-template yihua-app
$ cd yihua-app
$ yarn
$ yarn dev
```

## Reference

1. [Using the Notifications API](https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API/Using_the_Notifications_API), [MDN](https://developer.mozilla.org/en-US/)
2. [Notification](https://developer.mozilla.org/zh-TW/docs/Web/API/notification), [MDN](https://developer.mozilla.org/en-US/)
3. [Nuxt.js API Example using Vuex and axios](https://github.com/davidroyer/nuxt-api-example)
4. [Authentication module for Nuxt.js](https://github.com/nuxt-community/auth-module)