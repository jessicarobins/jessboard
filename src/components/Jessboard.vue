<template>
  <div class="container">
    <h1>Jessboard</h1>
    <div v-for="sound in sounds" class="sound" @click="play(sound.filename)">
      <h2>{{ sound.name }}</h2>
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
@import url('https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css');
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 80%;
}

.sound {
  border: 1px solid black;
  border-radius: 4px;
  padding: 20px;
  margin: 20px;
  height: 140px;
  width: 140px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #8A2BE2;
  color: white;
}

.sound:hover {
  cursor: pointer;
  background-color: #6317a9;
}

.sound:hover:before {
  content: "\f144";
  font-family: FontAwesome;
  position: absolute;
  font-size: 70px;
  opacity: 0.7;
  color: lightgray;
}

h1 {
  width: 100%;
  font-weight: 200;
  font-size: 72px;
}
</style>
