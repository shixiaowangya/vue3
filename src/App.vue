<template>
<div class="">
  <div class="">
    <h1>{{count}}</h1>
    <h1>{{duble}}</h1>
    <button @click="increase">按钮</button>
    <!-- <button @click="duble">按钮</button> -->
    <ul>
      <li v-for="item in numbers" :key="item">{{item}}</li>
    </ul>
    <h1>{{persom.name}}</h1>
  </div>
</div>
  
</template>
<script lang="ts">
import { ref, computed, reactive, toRefs } from "vue";
interface DateProps {
  count: number;
  duble: number;
  increase: () => void;
  numbers: number[];
  persom: { name?: string };
}
 
export default {
  name: "App",
  setup() {
    // const count = ref(0);
    // const duble = computed(() => {
    //   return count.value * 2;
    // }); 
    // const increase = () => {
    //   count.value++;
    // };
    const data: DateProps = reactive({
      count: 0,
      increase: () => {
        data.count++;
      },
      duble: computed(() => data.count * 2),
      numbers: [1, 2, 3],
      persom: {},
    });
    const refs = toRefs(data);
    data.numbers[0] = 5;
    data.persom.name = "prosm";
    return {
      // count,
      // increase,duble
      ...refs,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
