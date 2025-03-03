<template>
  <HomePage />
</template>

<script setup>
import HomePage from "./components/HomePage.vue";
</script>

<style>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  box-sizing: border-box;
}

html {
  width: 100%;
  height: 100%;
  position: relative;
  font-size: 16px;
}

body {
  width: 100%;
  height: 100%;
  overflow-x: hidden;
  -webkit-text-size-adjust: 100%;
  -webkit-tap-highlight-color: transparent;
}

#app {
  width: 100%;
  height: 100%;
  position: relative;
  margin: 0 auto;
}

img {
  max-width: 100%;
  height: auto;
}

/* 大屏幕设备 (4K及以上) */
@media screen and (min-width: 2560px) {
  html {
    font-size: 20px;
  }
  
  #app {
    max-width: 2400px;
  }
}

/* 标准桌面设备 */
@media screen and (max-width: 1440px) {
  html {
    font-size: 16px;
  }
}

/* 平板设备 */
@media screen and (max-width: 1024px) {
  html {
    font-size: 15px;
  }
}

/* 大屏手机 */
@media screen and (max-width: 768px) {
  html {
    font-size: 14px;
  }
}

/* 小屏手机 */
@media screen and (max-width: 480px) {
  html {
    font-size: 12px;
  }
}

/* 处理横屏情况 */
@media screen and (orientation: landscape) and (max-height: 768px) {
  html {
    font-size: 14px;
  }
}
</style>
