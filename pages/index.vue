<template>
  <section class="container">
    <div>
      <!-- <logo />
      <h1 class="title">
        nuxt-demo
      </h1>
      <h2 class="subtitle">
        FW
      </h2> -->
      <div class="links">
        <a class="button--green" >Documentation</a>
        <a class="button--green" v-for="item in list" :key="item.id">{{item.label}}</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >GitHub</a>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  data () {
    return {
      list: [
        { id: 0, label: 'w' },
        { id: 1, label: 'r' },
        { id: 2, label: 'f' }
      ]
    }
  },
  beforeCreate () {
    console.log(window)
    console.log(this)
    console.log('beforeCreate')
  },
  created () {
    console.log(this)
    console.log('create')
  },
  components: {
    Logo
  },

}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.button--green {
  margin: 0 20px;
}
</style>
