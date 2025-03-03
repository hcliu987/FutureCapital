<template>
  <div class="services" id="services">
    <div class="top">
      <div class="top-line"></div>
      <div class="top-item">
        <div class="top-title">Our Services</div>
        <div class="top-text">
          Assist the rental of of primary and secondary commercial/residential
          properties.
        </div>
        <div class="top-text">
          Assist the rental of of primary and secondary commercial/residential
          properties.
        </div>
      </div>
    </div>
    <div class="imgs">
      <img src="@/assets/services_bg1.png" />
      <img src="@/assets/services_bg2.png" />
    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.services {
  background: #fff;
  overflow: hidden;
}

.top {
  padding: 150px 120px 150px 150px;

  &-line {
    width: 466px;
    height: 1px;
    background: #987159;
    margin-bottom: 65px;
  }

  &-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 40px;
  }

  &-title {
    max-width: 550px;
    font-size: 80px;
  }

  &-text {
    max-width: 460px;
    font-size: 28px;
    line-height: 36px;
  }
}

.imgs {
  display: flex;
  width: 100%;

  & > img:first-child {
    width: 67%;
  }

  & > img:last-child {
    width: 33%;
  }
}

.services {
  @media (max-width: 1280px) {
    .top {
      padding: 20px;

      &-line {
        display: none;
      }

      &-item {
        text-align: center;
        justify-content: center;
        flex-direction: column;
      }

      &-title {
        font-size: 40px;
      }

      &-text {
        font-size: 18px;
      }
    }

    .imgs {
      flex-direction: column;

      & > img {
        width: 100%;
      }

      & > img:last-child {
        height: 200px;
      }
    }
  }
}

</style>
