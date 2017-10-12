<template id="news">
  <v-ons-page>
    <custom-toolbar title="News" :action="toggleMenu"></custom-toolbar>
    <p style="text-align: center">
      Some news here.
    </p>
  </v-ons-page>
</template>

<script>
import CustomToolbar from './CustomToolbar'

export default {
  name: 'News',
  props: ['toggleMenu'],
  components: {
    'custom-toolbar': CustomToolbar
  }
}
</script>
