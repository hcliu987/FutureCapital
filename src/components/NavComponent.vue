<template>
  <div class="nav">
    <div class="nav-left">
      <img class="nav-logo" src="@/assets/logo.png" />
    </div>
    <div class="nav-right">
      <ul class="nav-right-large">
        <li v-for="(item) in navConfig" :key="item.link">
          <a :href="item.link" :target="item.target">{{ item.text }}</a>
        </li>
      </ul>
      <div class="nav-right-small" @click="onShowNavMenu">
        <ul class="nav-right-small-icon">
          <li v-for="item in 3" :key="item" :data-item="item" />
        </ul>
        <Teleport to="body">
          <div v-if="isShowNavMenu" class="modal" @click="onShowNavMenu">
            <div class="modal-container">
              <ul class="modal-nav">
                <li v-for="(item) in navConfig" :key="item.link">
                  <a :href="item.link" :target="item.target">{{ item.text }}</a>
                </li>
              </ul>
            </div>
          </div>
        </Teleport>
      </div>
    </div>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  
  const isShowNavMenu = ref(false);
  const navConfig = [
    { text: 'Projects', link: 'https://future-capital.brokers.properties/en/', target: '_blank' },
    { text: 'Invest', link: '#invest' },
    { text: 'Services', link: '#services' },
    { text: 'Advantages', link: '#advantages' },
    { text: 'Contact Us', link: '#contactUs' },
  ];

  const onShowNavMenu = () => {
    isShowNavMenu.value = !isShowNavMenu.value;
    document.querySelector('body').setAttribute('style', `overflow: ${isShowNavMenu.value ? 'hidden' : 'auto'}`)
  }
</script>

<style lang="scss" scoped>
.modal {
  width: 100%;
  height: 100%;
  position: fixed;
  inset: 0;
  top: 60px;
  background-color: rgba(0,0,0,0.45);

  &-container {
    width: 200px;
    height: 100%;
    background-color: #fff;
    position: fixed;
    right: 0;
  }

  &-nav {
    padding: 20px;
    display: flex;
    flex-direction: column;

    & > li {
      text-align: center;
      margin-bottom: 20px;
      color: #987159;
      cursor: pointer;
      font-size: 16px;
      font-weight: bold;

      & > a {
        color: #987159;
        text-decoration: none;
      }
    }
  }
}
.nav {
  height: 60px;
  background: #f2f2f2;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 210px 0 85px;
  margin-bottom: 2px;
  position: sticky;
  top: 0;
  z-index: 99;

  &-left {
    display: flex;
    align-items: center;
  }

  &-logo {
    height: 26px;
  }
  
  &-right {
    &-large {
      display: flex;
      align-items: center;
      justify-content: end;
      width: 100%;
      font-family: 'Outfit Bold';

      & > li {
        margin-left: 45px;
        color: #987159;
        cursor: pointer;
        font-size: 16px;
        font-weight: bold;

        & > a {
          color: #987159;
          text-decoration: none;
        }
      }
    }

    &-small {
      display: none;

      &-icon {
        width: 20px;
        height: 14px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;

        & > li {
          width: 100%;
          height: 2px;
          background-color: #ccc;
        }

        & > li:nth-of-type(2) {
          width: 80%;
        }
      }
    }
  }
}

@media (max-width: 1280px) {
  .nav {
    padding: 0 20px;
  
    &-right {
      &-large {
        display: none;
      }

      &-small {
        display: block;
      }
    }
  }
}
</style>
