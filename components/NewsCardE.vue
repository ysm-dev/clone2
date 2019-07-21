<template>
  <div class="e">
    <div class="header">
      <img class="label"
           src="label_weather.svg" />
      <img class="button"
           src="button_circle.svg" />
    </div>
    <div class="content">
      <span>
        Vampires The Romantic Ideology Behind Them
      </span>
    </div>
    <div class="line" />
    <div class="footer">
      <span class="date">
        24 Jun, 5:40 PM
      </span>
      <div class="comments">
        <img src="ic_forum.svg"
             class="icon">
        <span class="count">
          12
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.line {
  background: #ffffff;
  opacity: 0.3;

  mix-blend-mode: normal;
}
.e {
  position: relative;
  display: grid;
  height: 240px;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%), url(../static/news5_img.png);
  background-position: 50% 50%;
  background-size: cover;
  background-repeat: no-repeat;
  color: white;

  grid-template-rows: 90px 1fr 2px 60px;
  grid-area: e;
  .header {
    display: block;
    border-radius: 6px 6px 0px 0px;

    .label {
      position: absolute;
      top: 20px;
      left: 20px;
    }
    .button {
      position: absolute;
      top: 20px;
      right: 20px;
      &:hover {
        border-radius: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        cursor: pointer;
      }
    }
  }
  .content {
    padding: 20px;
    padding-bottom: 18px;
    span {
      font-size: 16px;
      line-height: 25px;
    }
  }
  .footer {
    display: grid;
    align-content: center;
    align-items: center;
    font-size: 13px;
    line-height: 60px;

    grid-auto-flow: column;
    .date {
      margin-left: 20px;

      justify-self: start;
    }
    .comments {
      display: flex;
      padding: 0 20px;

      justify-self: end;
      .icon {
        margin-right: 15px;
      }
      .count {
        font-size: 12px;
      }
      &:hover {
        background-color: rgba(0, 0, 0, 0.5);
        cursor: pointer;
      }
    }
  }
}
</style>
