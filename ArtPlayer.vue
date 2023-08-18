<template>
    <div>
      <div class="artplayer-app"></div>
    </div>
  </template>
  
  <script setup>
  import { onMounted } from 'vue'
  import Artplayer from 'artplayer';
  
  // 获取传值 Get the props
  const props = defineProps(['src'])
  console.log(props.src)
  
  // 渲染播放器 Render player
  onMounted(() => {
    const art = new Artplayer({
      container: '.artplayer-app',
      url: props.src,
      theme: '#646cff',
      playbackRate: true,
      aspectRatio: true,
      screenshot: true,
      setting: true,
      pip: true,
      fullscreen: true,
      fullscreenWeb: true,
      airplay: true,
      // plugins: [
      //     artplayerPluginControl(),
      // ],
    });
  })
  </script>
  
  <style lang="scss" scoped>
  .artplayer-app {
    width: 800px;
    height: 450px;
    max-width: calc(100vw - 48px);
    max-height: calc(56.25vw - 27px);
  }
  </style>