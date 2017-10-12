<template id="news">
  <v-ons-page>
    <custom-toolbar title="News" :action="toggleMenu" :openSide="openSide" v-on:toggleMenu="sideMenu"></custom-toolbar>
    <p style="text-align: center">
      Some news here.
    </p>
  </v-ons-page>
</template>

<script>
import CustomToolbar from './CustomToolbar'

export default {
  name: 'News',
  props: ['toggleMenu', 'openSide'],
  components: {
    'custom-toolbar': CustomToolbar
  },
  methods: {
    sideMenu(isOpen) {
      this.$emit('toggleMenu', [isOpen]);
    }
  }
}
</script>
