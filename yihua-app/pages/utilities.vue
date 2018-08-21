<template lang="pug">
  v-layout
    v-flex(text-xs-center)
      h1.text-xs-left Utilities
      v-tabs(v-model='active', color='black', dark='', slider-color='white')
        v-tab(v-for='(item, index) in items', :key='n', ripple='')
          | {{ item.title }}
        v-tab-item(v-for='n in 6', :key='n')
          v-card(flat='')
            v-card-text {{ text }}
      //- v-menu(offset-y='')
      //-   v-btn(slot='activator', color='primary', dark='')
      //-     | Tools
      //-   v-list
      //-     v-list-tile(v-for='(item, index) in items', :key='index', @click='')
      //-       v-list-tile-title {{ item.title }}
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: 'HTML to Pug' },
      { title: 'JSON beautify' },
      { title: 'Translator' },
      { title: 'URL Shortener' },
      { title: 'Icons' },
      { title: 'Components' }
    ]
  })
}
</script>