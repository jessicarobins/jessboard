<template>
  <div class="container">
    <div v-for="sound in sounds" class="sound">
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
          name: "tony",
          filename: "tony.mp3"
        }, {
          name: "it's lunchtime",
          filename: "lunchtime.mp3"
        }, {
          name: "hey brian",
          filename: "brian.mp3"
        }, {
          name: "oh nooo",
          filename: "ohno.mp3"
        }, {
          name: "laters",
          filename: "laters.mp3"
        }, {
          name: "get outta here bear",
          filename: "bear.mp3"
        },{
          name: "hey you guys",
          filename: "heyyouguys.mp3"
        }, {
          name: "hi nathalie",
          filename: "nathalie.mp3"
        }, {
          name: "giggles"
        }, {
          name: "chuckle",
          filename: "chuckle.mp3"
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
}

.sound {
  border: 1px solid black;
  border-radius: 4px;
  padding: 20px;
  margin: 20px;
  height: 140px;
  width: 140px;
}
</style>
