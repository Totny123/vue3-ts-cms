<template>
  <div>
    <div>{{ store.state.name }}</div>
    <router-link to="/login">登录</router-link>
    <router-link to="/main">首页</router-link>
    <router-view></router-view>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { useStore } from 'vuex';

export default defineComponent({
  name: 'App',
  setup() {
    const store = useStore();
    return {
      store
    };
  }
});
</script>

<style lang="less">
#app {
  border: 1px solid red;
}
</style>
