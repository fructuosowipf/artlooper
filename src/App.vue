<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <vue-record-audio @result="onResult" />
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {

  },
  methods: {
    onResult (data) {
      console.log('The blob data:', data);
      console.log('Downloadable audio', window.URL.createObjectURL(data));
    }
  }
}
</script>

<style>

</style>
