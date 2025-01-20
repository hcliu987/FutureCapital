<template>
  <div class="invest" id="invest">
    <div class="top">
      <div class="top-title">New Opportunities</div>
      <div class="top-title">for Global Asset Allocation</div>
      <div class="top-line"></div>
    </div>
    <div class="middle">
      <div class="middle-item" v-for="(item) in itemConfig" :key="item.text">
        <div class="middle-item-pre">{{ item.proportion }}</div>
        <div class="middle-item-text">
          {{ item.text }}
        </div>
      </div>
    </div>
    <div class="bottom">
      <div class="bottom-text">
        Dubai, as a world-leading international metropolis, serves not only as
        the economic and trade hub of
      </div>
      <div class="bottom-text">
        the Middle East but also as a focal point for global investors.
      </div>
    </div>
  </div>
</template>

<script setup>
  const itemConfig = [
    { proportion: '0%', text: 'Tax Incentives: Zero personal income tax.Zero capital gains tax.' },
    { proportion: '6%-8%', text: 'Leading Investment Returns:The real estate market offers an average annual rental yield of 6%-8%.' },
    { proportion: '12%', text: 'High-End Residential Growth:Luxury residential projects boast an annual sales growth rate exceeding 12%.' },
    { proportion: '100%', text: 'Non-UAE investors can achieve 100% foreign ownership.' },
    { proportion: '80%', text: 'Over 80% of the population in Dubai consists of expatriates, leading to steadily growing housing demand.' },
    { proportion: '60%', text: 'Located at the intersection of Europe, Asia, and Africa, 60% of global markets are within an 8-hour flight radius.' },
  ]
</script>

<style lang="scss" scoped>
.invest {
  width: 100%;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.top {
  background: #fff;
  text-align: center;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  padding-top: 40px;
  padding-bottom: 20px;
  margin-bottom: 50px;

  &-title {
    font-size: 80px;
    color: #000;
    line-height: 80px;
    font-weight: 700;
    font-family: Outfit Bold;
  }

  &-line {
    height: 1px;
    background: #987159;
    width: 773px;
    margin-top: 32px;
  }
}

.middle {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  background: #f2f2f2;
  gap: 20px;
  padding: 90px 328px 30px 328px;

  &-item {
    display: flex;
    flex-direction: column;
    width: 314px;
    margin-bottom: 40px;

    &-pre {
      font-size: 80px;
      line-height: 80px;
      color: #987159;
      margin-bottom: 7.5px;
    }

    &-text {
      font-size: 20px;
      line-height: 25.2px;
      color: #000;
    }
  }
}


.bottom {
  width: 100%;
  text-align: center;
  background: #f2f2f2;
  padding-bottom: 10px;
  &-text {
    text-align: center;
    font-size: 28px;
    line-height: 36px;

    &:not(:last-child) {
      margin-bottom: 10px;
    }
  }
}

.invest {
  @media (max-width: 768px) {
    .top {
      padding-top: 30px;
      padding-bottom: 10px;
      margin-bottom: 20px;

      &-title {
        font-size: 20px;
        line-height: 30px;
      }

      &-line {
        display: none;
      }
    }

    .middle {
      padding: 20px;
      text-align: center;

      &-item {
        width: 100%;
        &:not(:last-child) {
          margin-bottom: 0;
        }

        &-pre {
          font-size: 40px;
          line-height: 40px;
        }

        &-text {
          font-size: 16px;
        }
      }
    }

    .bottom {
      &-text {
        padding-left: 20px;
        padding-right: 20px;
        font-size: 18px;
        line-height: 24px;
      }
    }
  }
}
</style>
