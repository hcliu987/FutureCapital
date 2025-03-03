<template>
  <div class="advantages" id="advantages">
    <div class="header">
      <div class="header-inner">
        <div class="header-container">
          Our Advantages
        </div>
      </div>
    </div>
    <ul class="content">
      <li class="content-item" v-for="(item) in itemConfig" :key="item.content">
        <div class="content-item-title">
          {{ item.title }}
        </div>
        <div class="content-item-info">
          {{ item.content }}
        </div>
      </li>
    </ul>
    <div class="img">
      <div class="img-inner" />
    </div>
  </div>
</template>

<script setup>
  const itemConfig = [
    { title: 'Company Introduction', content: 'A professional real estate consultancy team offering accurate market analysis and expert advice.' },
    { title: 'High-End Resource Integration', content: 'Collaborating with Dubai’s top developers, such as EMAAR, Nakheel, and DAMAC, to provide exclusive properties and premium resources.' },
    { title: 'Customer First', content: 'Placing client needs at the core, delivering full process, comprehensive support from property selection to investment implementation.' },
    { title: 'Global Perspective', content: 'Serving clients worldwide, including investors from China, the UK, India, Europe, and Gulf countries.' },
  ]
</script>

<style lang="scss" scoped>

.advantages {
  overflow: hidden;
  width: 100%;
  margin-top: 10px;
}

.header {
  width: 100%;

  &-inner {
    background-image: url('@/assets/advantages_bg1.jpg');
    background-repeat: no-repeat;
    background-size: 100% 100%;
    padding-top: 75%;
    height: 0;
    position: relative;
  }

  &-container {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%);
    font-size: 80px;
    color: #fff;
    white-space:nowrap;
  }
}

.content {
  margin-top: 50px;
  margin-bottom: 30px;
  padding: 63px 142px 0 172px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;

  &-item {
    display: flex;
    flex-direction: column;
    width: 345px;

    &-title {
      color: #987159;
      font-size: 28px;
      margin-bottom: 40px;
    }

    &-info {
      font-size: 28px;
    }
  }
}

.img {
  width: 100%;
    
  &-inner {
    background-image: url('@/assets/advantages_bg2.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
    height: 488px;
  }
}

.advantages {
  @media (max-width: 1280px) {
    .header-container {
      font-size: 30px;
    }

    .content {
      margin-top: 0;
      margin-bottom: 0;
      padding: 20px;
      flex-direction: column;

      &-item {
        justify-content: center;
        width: 100%;
        text-align: center;

        &-title {
          font-size: 22px;
          margin-bottom: 20px;
        }

        &-info {
          font-size: 18px;
        }
      }
    }

    .img-inner {
      padding-top: 75%;
      height: 0;
    }
  }
}
</style>
