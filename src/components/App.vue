<template>
  <div class="container app">
    <ListOne />
    <ListTwo />
  </div>
</template>

<script>
import ListOne from './ListOne';
import ListTwo from './ListTwo';

export default {
  name: 'App',
  components: {
    ListOne,
    ListTwo
  }
};
</script>

<style lang="scss">
  body {
    display: flex;
    align-items: center;
    height: 100vh;
  }


.app {
  display: flex;
  justify-content: center;
}
</style>
