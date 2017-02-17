<template>
  <div>
    <div v-for="sound in sounds">
      {{ sound.name }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'jessboard',
  data () {
    return {
      sounds: [{
          name: "tony"
        }, {
          name: "it's lunchtime"
        }, {
          name: "hey brian"
        }, {
          name: "oh nooo"
        }, {
          name: "laters"
        }, {
          name: "get outta here bear"
        },{
          name: "hey you guys"
        }, {
          name: "hi nathalie"
        }, {
          name: "giggles"
        }
      ]
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
