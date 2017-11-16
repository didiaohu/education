<template>
  <div id="app">
    <transition name="router-fade" mode="out-in">
      <keep-alive>
        <router-view/>
      </keep-alive>
    </transition>
    
  </div>
</template>
<style scoped>
  #app{
      background: #F3F5F7;
      max-width: 750px;
      margin: 0 auto;
  }
  .router-fade-enter-active, .router-fade-leave-active {
      transition: opacity .3s;
  }
  .router-fade-enter, .router-fade-leave-active {
      opacity: 0;
  }
</style>
