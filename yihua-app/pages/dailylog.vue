<template lang="pug">
  v-layout
    v-flex(xs12='', sm6='', offset-sm3='')
      v-card
        v-card-title(primary-title='')
          div
            h3.headline.mb-0 上傳圖檔
            div
              | 今天要先完成上傳圖檔的介面，讓檔案圖片能夠上傳到 localstack 的 s3 bucket 上。
        v-card-actions
          v-btn(flat='', color='orange') 關閉
          v-btn(flat='', color='orange') 縮小
      br
      v-card
        v-card-title(primary-title='')
          div
            h3.headline.mb-0 上傳圖檔
            div
              | 今天要先完成上傳圖檔的介面，讓檔案圖片能夠上傳到 localstack 的 s3 bucket 上。
        v-card-actions
          v-btn(flat='', color='orange') 關閉
          v-btn(flat='', color='orange') 縮小
          div.text-xs-right(style='width: 100%;')
            | 2018/08/21 08:16
</template>
