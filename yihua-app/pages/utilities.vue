<template lang="pug">
  v-layout
    v-flex(text-xs-center)
      h1.text-xs-left Utilities
      v-tabs(v-model='active', color='black', dark='', slider-color='white')
        v-tab(v-for='(item, index) in items', :key='index', ripple='')
          | {{ item.title }}
        v-tab-item(v-for='(item, index) in items', :key='index')
          v-card(flat='')
            v-card-text {{ item.title }}
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: 'AWS' },
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