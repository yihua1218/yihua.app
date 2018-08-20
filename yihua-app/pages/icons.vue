<template lang="pug">
  v-layout
    v-flex(text-xs-center)
      h1 Icons
      div
        v-btn(color='primary', dark='')
          | Accept
          v-icon(dark='', right='') check_circle
        v-btn(color='red', dark='')
          | Decline
          v-icon(dark='', right='') block
        v-btn(dark='')
          v-icon(dark='', left='') remove_circle
          | Cancel
      div
        v-btn(color='orange darken-2', dark='')
          v-icon(dark='', left='') arrow_back
          | Back
        v-btn(color='purple', dark='')
          v-icon(dark='') build
        v-btn(color='indigo', dark='')
          v-icon(dark='') backup
      div
        v-btn(flat='', icon='', color='blue lighten-2')
          v-icon thumb_up
        v-btn(flat='', icon='', color='red lighten-2')
          v-icon thumb_down
      div
        component(:is="goodshare")
</template>

<script>
export default {
  data: () => ({
    'goodshare': ''
  }),
  components: {
    VueGoodshare: () => import('vue-goodshare')
  },
  mounted() {
    this.goodshare = 'VueGoodshare'
  }
}
</script>