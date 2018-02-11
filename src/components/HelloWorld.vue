<template>
  <div class="hello">
    {{typeof(jsonData)}}
    <ul v-if="typeof(jsonData) === 'object'">
      <li v-for="prop in Object.keys(jsonData)" v-bind:prop="prop" :key="prop">
        {{prop}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  created () {
    window.vueBus.$on('jsonLoaded', json => {
      console.log(json)
      this.jsonData = json
    })
  },
  data () {
    return {
      jsonData: {
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
