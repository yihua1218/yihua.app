<template>
  <v-app dark>
    <v-navigation-drawer
      :mini-variant="miniVariant"
      :clipped="clipped"
      v-model="drawer"
      fixed
      app
    >
      <v-list>
        <v-list-tile
          router
          :to="item.to"
          :key="i"
          v-for="(item, i) in items"
          exact
        >
          <v-list-tile-action>
            <v-icon v-html="item.icon"></v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"></v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar fixed app :clipped-left="clipped">
      <v-toolbar-side-icon @click="drawer = !drawer"></v-toolbar-side-icon>
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon v-html="miniVariant ? 'chevron_right' : 'chevron_left'"></v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="clipped = !clipped"
      >
        <v-icon>web</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="fixed = !fixed"
      >
        <v-icon>remove</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer :fixed="fixed" app>
      <span>&copy; 2018 YiHua.App</span>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data() {
      return {
        clipped: false,
        drawer: true,
        fixed: false,
        items: [
          { icon: 'dashboard', title: 'Dashboard', to: '/' },
          { icon: 'apps', title: 'Functions', to: '/functions' },
          { icon: 'info', title: 'Serial Port', to: '/serialport' },
          { icon: 'history', title: 'Daily Log', to: '/dailylog' },
          { icon: 'build', title: 'Utilities', to: '/utilities' },
          { icon: 'settings', title: 'Settings', to: '/settings' },
          { icon: 'account_circle', title: 'Accounts', to: '/accounts' },
          { icon: 'contact_support', title: 'About', to: '/about' }
        ],
        miniVariant: false,
        right: true,
        rightDrawer: false,
        title: 'YiHua.App',
        isFBReady: false
      }
    },
    mounted: function () {
        this.isFBReady = Vue.FB != undefined
        window.addEventListener('fb-sdk-ready', this.onFBReady)
    },
    beforeDestroy: function () {
        window.removeEventListener('fb-sdk-ready', this.onFBReady)
    },
    methods: {
        onFBReady: function () {
          console.log('Facebook SDK ready.');
          this.isFBReady = true
        }
    }
  }
</script>
