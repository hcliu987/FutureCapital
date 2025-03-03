<template>
  <div class="aboutUs" id="aboutUs">
    <div class="aboutUs-1">
      <img class="aboutUs-1-logo" src="@/assets/aboutUs_logo.png" />
      <div class="aboutUs-1-title">Middle East Real</div>
      <div class="aboutUs-1-title">Estate Service Platform</div>
      <div class="aboutUs-1-subInfo">
        Tailor-made investment solutions with fullprocess
      </div>
      <div class="aboutUs-1-subInfo">support for asset appreciation.</div>
    </div>
    <div class="aboutUs-2">
    <div class="aboutUs-2-left"></div>
    <div class="aboutUs-2-right">
      <img src="@/assets/aboutUs_bg2.png" />
    </div>
    <div class="aboutUs-2-con_txt">
      <div class="aboutUs-2-con_txt-title">About us</div>
      <div class="aboutUs-2-con_txt-subtitle">Company Introduction</div>
      <div class="aboutUs-2-con_txt-intro">
        Future Capital is an international real estate consultancy and
        investment services company headquartered in Dubai. We specialize in
        providing comprehensive real estate investment solutions to clients
        worldwide. With deep market insights, a professional operations team,
        and robust resource integration capabilities, we assist clients in
        preserving and growing their assets in Dubai, one of the world’s
        hottest investment destinations.
      </div>
    </div>
  </div>
  <div class="aboutUs-3">
    <div class="aboutUs-3-left">
      <img src="@/assets/aboutUs_bg3.png" />
    </div>
    <div class="aboutUs-3-right"></div>
    <div class="aboutUs-3-con_txt">
      <div class="aboutUs-3-con_txt-title">Company Vision</div>
      <div class="aboutUs-3-con_txt-line"></div>
      <div class="aboutUs-3-con_txt-info">
        Whether you are looking for an ideal home or exploring high-yield
        investment opportunities, Future Capital is committed to a
        customer-first philosophy. <br /><br />
        We deliver tailored investment support through exceptional service
        quality and forward-thinking market analysis, ensuring a personalized
        experience for every client.
      </div>
    </div>
  </div>
  </div>  
</template>

<script setup>
</script>

<style lang="scss" scoped>
.aboutUs {
  width: 100%;
  position: relative;
  margin-bottom: 2px;
  overflow: hidden;
}

.aboutUs-1 {
  height: 100%;
  min-height: 1080px;
  background-image: url('@/assets/aboutUs_bg1.jpg');
  background-repeat: no-repeat;
  background-size: 100% 100%;
  padding-top: 160px;
  padding-left: 224px;

  &-logo {
    width: 180px;
    height: auto;
    position: relative;
    z-index: 1;
    margin-bottom: 12px;
  }

  &-title {
    font-size: 66px;
    font-weight: 700;
    color: #000;
    line-height: 80px;
    position: relative;
    z-index: 1;
    font-family: Outfit Bold;
  }

  &-subInfo {
    font-size: 28px;
    line-height: 36px;
    position: relative;
    z-index: 1;

    &:first-child {
      margin-top: 8px;
    }
  }
}

.aboutUs-2 {
  display: flex;
  width: 100%;
  min-height: 1080px;
  position: relative;
  margin-bottom: 2px;

  &-left {
    width: 33%;
    background: #fff;
  }

  &-right {
    width: 67%;
    background: #f2f2f2;
    text-align: right;

    img {
      max-width: 82.5%;
    }
  }

  &-con_txt {
    position: absolute;
    top: 260px;
    left: 270px;
    width: 573px;

    &-title {
      font-size: 80px;
      line-height: 80px;
      color: #000;
    }

    &-subtitle {
      font-size: 28px;
      color: #987159;
      line-height: 36px;
      margin: 30px 0;
    }

    &-intro {
      font-size: 28px;
      line-height: 36px;
      font-family: 'outFit Light';
    }
  }
}

.aboutUs-3 {
  display: flex;
  width: 100%;
  position: relative;
  margin-bottom: 2px;
  background: #f2f2f2;

  &-left {
    width: 55.7%;
  }

  &-right {
    width: 44.3%;
    background: #f2f2f2;
  }

  &-con_txt {
    width: 851px;
    height: 678px;
    background: #fff;
    position: absolute;
    top: 110px;
    right: 110px;
    padding: 182px 0 0 132px;
    border-radius: 5%;

    &-title {
      font-size: 28px;
      color: #987159;
      line-height: 36px;
      margin-bottom: 66px;
      font-weight: 700;
      font-family: Outfit Bold;
    }

    &-line {
      height: 1px;
      width: 145px;
      margin-bottom: 38px;
      background: #987159;
    }

    &-info {
      width: 533px;
      font-size: 28px;
      line-height: 36px;
    }
  }
}

.aboutUs {
  @media (max-width: 1280px) {
    .aboutUs-1 {
      padding: 20px;
      min-height: inherit;

      &-logo {
        width: 50px;
        height: 50px;
        margin-bottom: 0;
      }

      &-title {
        font-size: 20px;
        line-height: 30px;
      }

      &-subInfo {
        font-size: 18px;
        line-height: 16px;
      }
    }

    .aboutUs-2 {
      min-height: 800px;

      &-con_txt {
        width: 100%;
        text-align: center;
        left: 50%;
        transform: translateX(-50%);

        &-title {
          font-size: 40px;
        }

        &-subtitle {
          margin: 10px 0;
        }

        &-intro {
          padding: 0 20px;
          font-size: 18px;
        }
      }
    }

    .aboutUs-3 {
      &-right {
        display: none;
      }

      &-left {
        width: 100%;
      }
      &-con_txt {
        height: auto;
        padding: 20px;
        inset: 0;
        top: 50%;
        left: 20px;
        right: 20px;
        transform: translateY(-50%);
        width: calc(100% - 80px); 

        &-title {
          font-size: 20px;
          margin-bottom: 20px;
        }

        &-line {
 
          margin-bottom: 20px;
        }

        &-info {
          width: 100%;
          font-size: 18px;
        }
      }
    }
  }
}
</style>
