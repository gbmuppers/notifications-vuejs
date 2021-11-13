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
  mounted(){
    let notification = new Notification('Hola, esta es una notifiación',{ body: 'Love u'})
    window.navigator.vibrate(1000)
    notification.onclick = function(event) {
      event.preventDefault(); // Previene al buscador de mover el foco a la pestaña del Notification
      window.open('http://www.mozilla.org', '_blank');
    }
  },
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
