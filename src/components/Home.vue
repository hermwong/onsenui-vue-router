<template id="home">
  <v-ons-page>
    <custom-toolbar title="Home" :action="toggleMenu" :openSide="openSide" v-on:toggleMenu="sideMenu"></custom-toolbar>
    <p style="text-align: center">
      Welcome home.
    </p>
  </v-ons-page>
</template>

<script>
import CustomToolbar from './CustomToolbar'

export default {
  name: 'Home',
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
