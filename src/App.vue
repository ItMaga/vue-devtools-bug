<template>
  <div id="app">
    <VueDraggable :list="list1" group="test" :noTransitionOnDrag="true">
      <transition-group name="card-transition">
        <Card v-for="item of list1" :key="item.id" :title="item.title" />
      </transition-group>
    </VueDraggable>
    <VueDraggable :list="list2" group="test" :noTransitionOnDrag="true">
      <transition-group name="card-transition">
        <Card v-for="item of list2" :key="item.id" :title="item.title" />
      </transition-group>
    </VueDraggable>
  </div>
</template>

<script>
import VueDraggable from 'vuedraggable';
import Card from "@/components/Card";

export default {
  name: 'App',

  components: {Card, VueDraggable },

  data: () => ({
    list1: [
      {
        id: 1,
        title: 'Item 1',
      },
      {
        id: 2,
        title: 'Item 2',
      }
    ],
    list2: [
      {
        id: 3,
        title: 'Item 3',
      },
      {
        id: 4,
        title: 'Item 4',
      }
    ]
  })
}
</script>

<style>
#app {
  display: flex;
  align-items: center;
  justify-content: center;
  column-gap: 50px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.card-transition-move {
  transition: transform 0.3s;
}
</style>
