<template>
  <div id="app">
      <b-card>
        <b-button variant="primary" @click="swap()">Json Değiş</b-button>
        <b-card>
        <b-card-text v-for="nesne in contentJson" :key="nesne">{{nesne}}</b-card-text>
        </b-card>
      </b-card>
  </div>
</template>

<script>
import unixfsJson from './json/unixfs.json'
import youtubeJson from './json/youtube.json'

export default{
    data(){
      return{
        contentJson : unixfsJson,
        altJson : youtubeJson,
        tmp : ""
      }
    },
    methods:{
      swap(){
        this.tmp = this.contentJson,
        this.contentJson = this.altJson,
        this.altJson = this.tmp
      }
    }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
