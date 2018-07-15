<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div id="img_canvas">
      <!-- <img id="camanjs" src="https://tpc.googlesyndication.com/daca_images/simgad/8454867233327495675" crossorigin="anonymous"/>
      -->
    </div>
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a
          href="https://vuejs.org"
          target="_blank"
        >
          Core Docs
        </a>
      </li>
      <li>
        <a
          href="https://forum.vuejs.org"
          target="_blank"
        >
          Forum
        </a>
      </li>
      <li>
        <a
          href="https://chat.vuejs.org"
          target="_blank"
        >
          Community Chat
        </a>
      </li>
      <li>
        <a
          href="https://twitter.com/vuejs"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <br>
      <li>
        <a
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
          Docs for This Template
        </a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a
          href="http://router.vuejs.org/"
          target="_blank"
        >
          vue-router
        </a>
      </li>
      <li>
        <a
          href="http://vuex.vuejs.org/"
          target="_blank"
        >
          vuex
        </a>
      </li>
      <li>
        <a
          href="http://vue-loader.vuejs.org/"
          target="_blank"
        >
          vue-loader
        </a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/awesome-vue"
          target="_blank"
        >
          awesome-vue
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  mounted () {
    console.log('loaded...')

    let imgCanvas = document.getElementById('img_canvas')
    let image = new Image()
    image.crossOrigin = 'anonymous'
    image.onload = function () {
      console.log('img loaded')
      console.log(imgCanvas)
      imgCanvas.appendChild(image)
      Caman(image, function () {
        // use selected preset, or do whatever you want here
        this.render(function () {
          // var dataUrl = div.querySelector ('canvas').toDataURL ('image/jpeg', 0.6);
        })
      })
    }
    image.src = 'https://tpc.googlesyndication.com/daca_images/simgad/8454867233327495675'

    // Caman('#camanjs', function () {
    //   this.brightness(100).render()
    // })
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
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
