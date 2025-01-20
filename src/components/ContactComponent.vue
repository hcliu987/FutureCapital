<template>
  <div class="contact" id="contactUs">
    <div class="left">
      <img src="@/assets/contact_bg2.png" />
    </div>
    <div class="right">
      <img src="@/assets/contact_bg1.png" />
    </div>
    <div class="content">
      <div class="content-title">
        <img src="@/assets/aboutUs_logo.png" />
        <div class="content-text">Contact us</div>
      </div>
      <div class="content-info">
        Thank you for your interest and trust in us! For more information
        about our projects or to discuss any inquiries and collaboration
        opportunities, feel free to reach out to our professional team. You
        can contact us through the following channels, and we look forward to
        providing you with the best service.
      </div>
      <div class="content-detail">
        <div class="content-detail-label">Phone</div>
        <div class="content-detail-value">+971 50 350 8883</div>
      </div>
      <div class="content-detail">
        <div class="content-detail-label">Email</div>
        <div class="content-detail-value">michael@futurecapital.ae</div>
      </div>
      <div class="content-detail">
        <div class="content-detail-label">Address</div>
        <div class="content-detail-value">
          3rd Floor Westburry Tower, Al Abraj Street Business Bay, Dubai
        </div>
      </div>
      <div class="content-end">
        We look forward to working with you to build a better future !
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>

.contact {
  display: flex;
  position: relative;
}

.left {
  background: #f2f2f2;
  width: 50%;
  display: flex;
  align-items: center;

  img {
    max-width: 22%;
    position: relative;
    z-index: 1;
  }
}

.right {
  width: 50%;
  background: #987159;
  display: flex;
  align-items: center;
  justify-content: end;

  img {
    max-width: 60%;
  }
}

.content {
  width: 40%;
  position: absolute;
  top: 108px;
  left: 200px;
  background: #fff;
  padding: 70px;
  border-radius: 10%;

  &-title {
    display: flex;
    align-items: flex-end;
  }

  &-info {
    font-size: 18px;
    line-height: 25px;
    margin-bottom: 50px;
    margin-top: 60px;
  }

  &-detail {
    display: flex;
    font-size: 18px;

    &-label, &-value{
      min-width: 119px;
      font-size: 15px;
      line-height: 30px;  
    }

    &-label {
      color: #000;
    }

    &-value {
      color: #987159;
    }
  }

  img {
    width: 18%;
    height: 18%;
  }

  &-text {
    font-size: 50px;
    margin-left: 93px;
    font-weight: 700;
    font-family: Outfit Bold;
  }

  &-end {
    font-size: 18px;
    line-height: 36px;
    text-align: center;
    margin-top: 50px;
  }
}

.contact {
  @media (max-width: 1280px) {
    .left, .right {
      display: none;
    }

    .content {
      width: 100%;
      padding: 20px;
      position: relative;
      inset: 0;

      &-title {
        img {
          width: 12%;
          height: 12%;
        }
      }

      &-info {
        margin-top: 30px;
        margin-bottom: 30px;
        text-align: center;
      }

      &-text {
        font-size: 24px;
        margin-left: 20px;
      }

      &-end {
        margin-top: 10px;
      }
    }
  } 
}
</style>
