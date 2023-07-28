<template>
  <div class="d-flex">
    <SideBar :isTrue="isTrue"/>
    <div class="header-body-div">
      <AppHeader @hideShowSidebar = 'hideShowSidebar'/>
      <Dashboard/>
    </div>
  </div>
</template>

<script>
import SideBar from '../src/components/SideBar/index.vue'
import AppHeader from './components/AppHeader.vue';
import Dashboard from '../src/components/Dashboard/index.vue'
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
    Dashboard
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
.header-body-div{
  width: 100%;
}
</style>
