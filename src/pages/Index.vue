<template>
  <q-page class="flex flex-center column">
    <vue-simple-suggest
      v-model="chosen"
      :list="simpleSuggestionList"
      :filter-by-query="true">
    </vue-simple-suggest>
    <p>Chosen element: {{ chosen }}</p>
  </q-page>
</template>

<script>
import VueSimpleSuggest from 'vue-simple-suggest'
import 'vue-simple-suggest/dist/styles.css'

export default {
  name: 'PageIndex',
  components: {
    VueSimpleSuggest
  },
  data () {
    return {
      chosen: '',
      items: ['Celular', 'Carro', 'Relógio', 'Pente', 'Buzina', 'Sabão']
    }
  },
  methods: {
    simpleSuggestionList () {
      return this.items
    }
  }
}
</script>
