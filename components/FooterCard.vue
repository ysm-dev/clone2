<template>
  <footer>
    <div class="top">
      <div class="menu">
        <span v-for="item in ['Food', 'Look', 'Digital','Design','Art']"
              :key="item">
          {{ item }}
        </span>
      </div>
      <div class="social">
        <div class="icon"
             v-for="item in ['twitter','instagram','facebook','youtube']"
             :key="item">
          <img :src="`${item}.svg`" />
        </div>
      </div>
    </div>
    <div class="line" />
    <div class="bottom">
      <span v-for="item in ['© 2016. Quantum UI kit', 'Privacy Policy', 'Terms of Use']"
            :key="item">
        {{ item }}
      </span>
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.line {
  background-color: #f5f5f5;
}
footer {
  display: grid;
  height: 330px;
  background-color: white;

  grid-template-rows: 1fr 2px 5.625rem;
  .top {
    display: flex;
    align-items: space-around;
    flex-direction: column;
    justify-content: space-evenly;
    color: #999999;
    font-size: 16px;
    line-height: 30px;
    .menu {
      text-align: center;
      span {
        padding: 5px 20px;
        &:hover {
          background-color: rgba(0, 0, 0, 0.05);
          cursor: pointer;
        }
      }
    }
    .social {
      display: flex;
      justify-content: center;
      .icon {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0px 20px;
        width: 50px;
        height: 50px;
        border: 2px solid #f5f5f5;
        border-radius: 100%;
        img {
          position: absolute;
        }
        &:nth-child(3) {
          padding-right: 1px;
        }
        &:hover {
          background-color: rgba(0, 0, 0, 1);
          cursor: pointer;
        }
      }
    }
  }
  .bottom {
    display: flex;
    justify-content: center;
    span {
      align-self: center;
      padding: 10px 20px;
      color: #b3b3b3;
      font-size: 14px;
      line-height: 30px;
      &:hover {
        background-color: rgba(0, 0, 0, 0.05);
        cursor: pointer;
      }
    }
  }
}
</style>
