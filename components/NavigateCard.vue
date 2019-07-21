<template>
  <header>
    <div class="top">
      <div class="left">
        <div class="city">
          <span>
            Bergstromtown
          </span>
          <img class="icon"
               src="ic_keyboard_arrow_down.svg" />
        </div>
        <div class="weather">
          <img class="icon"
               src="ic_weather.svg" />
          <span>
            +8°C
          </span>
        </div>
      </div>
      <img class="logo"
           src="logo.svg" />
      <div class="login">
        <img class="icon"
             src="ic_account_circle.svg" />
        <span>
          Sign in
        </span>
      </div>
    </div>
    <div class="line" />
    <div class="bottom">
      <div class="menu">
        <img class="icon"
             src="ic_menu.svg" />
      </div>
      <div class="line" />
      <div class="navigate">
        <div class="item"
             v-for="item in ['City', 'People','Business', 'Entertainment', 'Food', 'Style','Children']"
             :key="item">
          {{ item }}
        </div>
      </div>
      <div class="line" />
      <div class="search">
        <img class="icon"
             src="ic_search.svg" />
      </div>
    </div>
  </header>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
header {
  position: fixed;
  display: grid;
  min-width: 100%;
  width: 100%;
  height: 11.25rem;
  background-color: white;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);

  grid-template-rows: 1fr 2px 1fr;
  z-index: 1;
  .top {
    position: relative;
    display: grid;
    min-width: 100%;

    grid-auto-flow: column;
    .left {
      position: absolute;
      display: flex;
      height: 100%;
      .city {
        display: flex;
        padding-right: 1rem;
        padding-left: 1.875rem;
        height: 100%;
        span {
          align-self: center;
          width: 6.25rem;
          color: #999999;
          font: normal 500 0.875rem/30px Roboto;
        }
        .icon {
          margin-left: 3px;
        }
        &:hover {
          background-color: rgba(0, 0, 0, 0.05);
          cursor: pointer;
        }
      }
      .weather {
        display: flex;
        padding: 0 1.875rem;
        height: 100%;
        .icon {
        }
        span {
          align-self: center;
          margin-left: 15px;
          color: #666666;
          font: normal 500 0.875rem/30px Roboto;
        }
        &:hover {
          background-color: rgba(0, 0, 0, 0.05);
          cursor: pointer;
        }
      }
    }
    .logo {
      position: absolute;
      align-self: center;

      justify-self: center;
      &:hover {
        cursor: pointer;
      }
    }
    .login {
      position: absolute;
      display: flex;
      align-self: center;
      padding-right: 2.625rem;
      padding-left: 1.875rem;
      height: 100%;

      justify-self: end;
      span {
        align-self: center;
        margin-left: 10px;
        color: #999999;
        font: normal 500 0.875rem/30px Roboto;
      }
      .icon {
      }
      &:hover {
        background-color: rgba(0, 0, 0, 0.05);
        cursor: pointer;
      }
    }
  }
  & > .line {
    background-color: #f5f5f5;
  }
  .bottom {
    position: relative;
    display: grid;
    min-width: 100%;

    grid-template-columns: 89px 2px 1fr 2px 89px;
    .menu {
      z-index: 1;
      display: flex;
      justify-content: center;
      width: 89px;
      height: 100%;
      background-color: white;
      .icon {
      }
      &:hover {
        background-color: rgba(0, 0, 0, 0.05);
        cursor: pointer;
      }
    }
    & > .line {
      width: 2px;
      background-color: #f5f5f5;
    }
    .navigate {
      display: grid;
      overflow-x: hidden;
      justify-content: center;
      height: 100%;
      color: #999999;
      font-size: 14px;

      justify-self: center;
      grid-auto-flow: column;
      .item {
        display: flex;
        align-items: center;
        padding: 0 25px;
        height: 100%;
        &:hover {
          background-color: rgba(0, 0, 0, 0.05);
          cursor: pointer;
        }
      }
    }
    .search {
      display: flex;
      justify-content: center;
      width: 89px;
      height: 100%;
      background-color: white;

      justify-self: end;
      .icon {
      }
      &:hover {
        background-color: rgba(0, 0, 0, 0.05);
        cursor: pointer;
      }
    }
  }
}
</style>
