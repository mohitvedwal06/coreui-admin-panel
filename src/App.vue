<template>
  <div class="d-flex">
    <SideBar :isTrue="isTrue"/>
    <AppHeader @hideShowSidebar = 'hideShowSidebar'/>
  </div>
</template>

<script>
import SideBar from '../src/components/SideBar/index.vue'
import AppHeader from './components/AppHeader.vue';

export default {
  name: 'App',
  data() {
    return {
      isTrue: null,
    }
  },
  components: {
    SideBar,
    AppHeader,
  },
  methods: {
    hideShowSidebar(value){
      this.isTrue = value.isTrue;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
