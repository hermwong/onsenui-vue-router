<template id="home">
  <v-ons-page>
    <custom-toolbar title="Home" :action="toggleMenu"></custom-toolbar>
    <p style="text-align: center">
      Welcome home.
    </p>
  </v-ons-page>
</template>

<script>
import CustomToolbar from './CustomToolbar'

export default {
  name: 'Home',
  props: ['toggleMenu'],
  components: {
    'custom-toolbar': CustomToolbar
  }
}
</script>
