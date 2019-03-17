<template>
  <draggable
    class="list-group"
    v-model="listData1"
    group="items"
    @start="drag = true"
    @end="drag = false"
  >
    <div class="list-group-item" v-for="element in listData1" :key="element.id">
      {{ element.name }}
    </div>
  </draggable>
</template>

<script>
import draggable from 'vuedraggable';
import { listData1 } from '../data/list-data';

export default {
  name: 'ListOne',
  components: {
    draggable
  },
  data() {
    return {
      listData1
    };
  }
};
</script>

<style lang="scss">
.list-group {
  width: 37%;
  margin: 20px;
  height: 600px;
  .list-group-item {
    cursor: grab;
    &:active {
      cursor: grabbing;
    }
    &:hover {
      background-color: #eee;
    }
  }
}
</style>
