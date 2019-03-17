<template>
  <draggable
    class="list-group"
    v-model="listData2"
    group="items"
    @start="drag = true"
    @end="drag = false"
  >
    <div class="list-group-item" v-for="element in listData2" :key="element.id">
      {{ element.name }}
    </div>
  </draggable>
</template>

<script>
// import ListItem from './ListItem';
import draggable from 'vuedraggable';
import { listData2 } from '../data/list-data';

export default {
  name: 'ListTwo',
  components: {
    draggable
  },
  data() {
    return {
      listData2
    }
  }
};
</script>

<style>
</style>
