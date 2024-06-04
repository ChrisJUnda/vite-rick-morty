<script>

import AppHeaderTitle from './Components/AppHeaderTitle.vue';

import AppMainSearch from './Components/AppMainSearch.vue';

import AppMainFoto from './Components/AppMainFoto.vue';

import axios from 'axios';

import { store } from './store.js';





export default {
  name: 'AppRickMorty',
  components: {
    AppHeaderTitle,
    AppMainSearch,
    AppMainFoto,
  },
  data() {
    return {
      store,
      cards: []
    };
  },
  methods: {


    cardsGenerate() {
      axios.get("https://rickandmortyapi.com/api/character").then(response => {
        this.cards.push(response.data)
      })
    }
  },

  created() {
    axios.get(this.store.apiUrl).then((response) => {
      this.store.results = response.data.results
      this.store.info = response.data.info
    })
  }
};
</script>

<template>
  <AppHeaderTitle />
  <AppMainFoto />
  <AppMainSearch />
</template>
<!-- <style></style> -->
