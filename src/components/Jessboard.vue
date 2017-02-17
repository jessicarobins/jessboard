<template>
  <div class="container">
    <div v-for="sound in sounds" class="sound" @click="play(sound.filename)">
      {{ sound.name }}
    </div>
  </div>
</template>

<script>

var tony = require('../assets/tony.mp3')

export default {
  name: 'jessboard',
  data () {
    return {
      sounds: [{
          name: "tony",
          filename: "tony",
        }, {
          name: "it's lunchtime",
          filename: "lunchtime"
        }, {
          name: "hey brian",
          filename: "brian"
        }, {
          name: "oh nooo",
          filename: "ohno"
        }, {
          name: "laters",
          filename: "laters"
        }, {
          name: "get outta here bear",
          filename: "bear"
        },{
          name: "hey you guys",
          filename: "heyyouguys"
        }, {
          name: "hi nathalie",
          filename: "nathalie"
        }, {
          name: "giggles"
        }, {
          name: "chuckle",
          filename: "chuckle"
        }
      ]
    }
  },
  methods: {
    play: function(sound) {
      const fileName = require(`../assets/${sound}.mp3`)
      const audio = new Audio(fileName)
      audio.play()
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
