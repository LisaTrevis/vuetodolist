<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from './components/layout/Header'
export default {
  name: 'app',
  components: {
    Header
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
  /* COLOR PALETTE */
  /* #826BFF */
  /* #5176E8 */
  /* #B8C7FF */
  /* #51E8E5 */
  /* #59FFB8 */
</style>
