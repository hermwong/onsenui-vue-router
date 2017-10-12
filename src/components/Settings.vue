<template id="settings">
  <v-ons-page>
    <custom-toolbar title="Settings" :action="toggleMenu"></custom-toolbar>
    <p style="text-align: center">
      Change the settings.
    </p>
  </v-ons-page>
</template>

<script>
import CustomToolbar from './CustomToolbar'

export default {
  name: 'Settings',
  props: ['toggleMenu'],
  components: {
    'custom-toolbar': CustomToolbar
  }
}
</script>
