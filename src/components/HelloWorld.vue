<template>
  <div class="container">
    <h1>Hola mundo</h1>
    <h3>esta es mi primera pagina web</h3>
    <button type="button" @click="notify">Show notification</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    notify () {
      // https://developer.mozilla.org/en-US/docs/Web/API/Notification/Notification#Parameters
      this.$notification.show('Hello World', {
        body: 'This is an example!'
      }, {})
    }
  }
}
</script>
