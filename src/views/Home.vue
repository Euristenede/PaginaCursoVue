<template>
  <b-container>
    <b-row align-v="center">
      <card v-for="curso in cursos" 
            :key="curso.id" 
            :nome="curso.name" 
            :linkimg="curso.linkimg"
            :descricao="curso.descricao"></card>
    </b-row>
  </b-container>
</template>

<script>
// @ is an alias to /src
import Card from '../components/Card.vue'

export default {
  name: 'Home',
  data(){
    return{
      cursos: []
    }
  },
  components: {
    Card
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      const resultado = await fetch("cursos.json")
      const valor = await resultado.json();
      this.cursos = valor;
    }
  }
}
</script>
