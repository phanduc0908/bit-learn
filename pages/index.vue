<template>
  <div class="main">
    <div class="header">
      <div class="logo">
        <a href="https://bitscreener.com/">
          <img src="@/assets/images/bitscreener-logo.svg" alt="logo">
        </a>
      </div>
      <div class="title">
        Learn Technical Analysis
      </div>
    </div>
    <div class="container">
      <div v-for="(item, index) in data" :key="index" class="menu">
        <div class="row-item">
          <a href="#">
            <div class="section">
              <img :class="['logo', getLogo(item.menu1.isActive)]" src="@/assets/images/ic_section1.png" alt="img" width="100%">
              <div>{{item.menu1.text}}</div>
            </div>
          </a>
        </div>
        <div class="row-item">
          <a href="#">
            <div class="section-col">
              <img :class="['logo', getLogo(item.menu2.isActive)]" src="@/assets/images/ic_section1.png" alt="img">
              <div>{{item.menu2.text}}</div>
            </div>
          </a>
          <a href="#">
            <div class="section-col">
              <img :class="['logo', getLogo(item.menu3.isActive)]" src="@/assets/images/ic_section1.png" alt="img">
              <div>{{item.menu3.text}}</div>
            </div>
          </a>
        </div>
        <div class="row-item">
          <a href="#">
            <div class="section">
              <img class="logo test" src="@/assets/images/ic_section1.png" alt="img">
              <div>{{item.test.text}}</div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TestSVG from '@/assets/images/test-exam.svg?inline';
export default {
  components: {
    TestSVG
  },
  data() {
    return {
      data: [
        {
          menu1: {
            isActive: true,
            text:'Breakout and Dead Cat Bounce'
          },
          menu2: {
            isActive: false,
            text: 'Dow Theory',
          },
          menu3: {
            isActive: false,
            text: 'Market Trend',
          },
          test: {
            isActive: true,
            text: 'Summarized Test'
          }
        },
        {
          menu1: {
            isActive: false,
            text:'Support and Resistance'
          },
          menu2: {
            isActive: false,
            text: 'Money Flow Index and Relative Strength Index',
          },
          menu3: {
            isActive: false,
            text: 'Stochastic Oscillator and Stochastic Divergence',
          },
          test: {
            isActive: true,
            text: 'Summarized Test'
          }
        },
        {
          menu1: {
            isActive: false,
            text:'True Strenth Index, The Ultimate Oscillator and Williams %R'
          },
          menu2: {
            isActive: false,
            text: 'Average Directional Movement Index',
          },
          menu3: {
            isActive: false,
            text: 'Commodity Channel Index',
          },
          test: {
            isActive: true,
            text: 'Summarized Test'
          },
        },
        {
          menu1: {
            isActive: false,
            text:'Detrended Price Oscillator'
          },
          menu2: {
            isActive: false,
            text: 'KST Oscillator and MACD',
          },
          menu3: {
            isActive: false,
            text: 'Mass Index and Moving Average',
          },
          test: {
            isActive: true,
            text: 'Summarized Test'
          },
        },
        {
          menu1: {
            isActive: false,
            text:'Parabolic SAR and Smart Money Index'
          },
          menu2: {
            isActive: false,
            text: 'Trend Line and Trix Indicator',
          },
          menu3: {
            isActive: false,
            text: 'Average True Range and Bollinger Bands',
          },
          test: {
            isActive: true,
            text: 'Summarized Test'
          },
        },
      ]
    }
  },

  methods: {
    getLogo(isActive) {
      return isActive ? 'active' : 'locked'
    }
  }
}
</script>

<style lang="scss">
$unit : 8px;
.main {
  .header {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 70px;
    width: 100%;
    background-color: #0e4d90;
    position: fixed;
    .logo {
      width: 25px;
      height: 25px;
    }
    .title {
      padding-left: 5px;
      font-size: 19px;
      color: #ffffff;
      font-weight: 700;
    }
  }
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-bottom: 100px;
    .row-item {
      display: flex;
      justify-content: space-evenly;
      padding-top: 15px;
      .logo {
        width: 80px;
        height: 80px;
        border-radius: 50%;
        border: 3px solid #d8d9d9;
      }
      .section {
        display: flex;
        flex-direction: column;
        align-items: center;
      }
      .section-col {
        text-align: center;
      }
    }
    .menu {
      padding-top: 100px;
    }
  }
  .active {
    background-color: #5581b4;
  }
  .locked {
    background-color: #afb8c2;
  }
  .test {
    background-color: #e7b559;
  }
  a {
    text-decoration: none;
    color: #111;
  }
}

</style>
