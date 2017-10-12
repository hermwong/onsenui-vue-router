<template>
  <v-ons-splitter>
    <v-ons-splitter-side swipeable width="150px" collapse"" side="left" :open.sync="openSide" @click="doSomething">
      <v-ons-page>
        <v-ons-list>
          <v-ons-list-item v-for="page in pages" tappable modifier="chevron" @click="currentPage = page; openSide = false">
            <div class="center">{{ page }}</div>
          </v-ons-list-item>
        </v-ons-list>
      </v-ons-page>
    </v-ons-splitter-side>
    <v-ons-splitter-content>
      <component :is="currentPage" :toggle-menu="() => openSide = !openSide"></component>
    </v-ons-splitter-content>
  </v-ons-splitter>
</template>

<script>
import Home from './Home'
import Toolbar from './CustomToolbar'
import News from './News'
import Settings from './Settings'

export default {
  name: 'LeftMenu',
  props: ['title', 'action'],
  components: {
    home: Home,
    'custom-toolbar': Toolbar,
    news: News,
    settings: Settings
  },
  data() {
    return {
      currentPage: 'home',
      pages: ['home', 'news', 'settings'],
      openSide: false
    }
  },
  methods: {
    doSomething() {
      console.log(openSide);
    }
  }
}
</script>
