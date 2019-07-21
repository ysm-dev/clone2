<template>
  <div class="i">
    <div class="header">
      <img class="label"
           src="label_news.svg" />
      <img class="button"
           src="button_circle.svg" />
    </div>
    <div class="content">
      <span>
        E Banks That Accept Us Casino Players
      </span>
    </div>
    <div class="line" />
    <div class="footer">
      <span class="date">
        24 Jun, 5:40 PM
      </span>
      <div class="comments">
        <img src="ic_forum_gray.svg"
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
  background-color: #f5f5f5;
}
.i {
  position: relative;
  display: grid;
  height: 330px;

  grid-template-rows: 180px 1fr 2px 60px;
  grid-area: i;
  .header {
    display: block;
    border-radius: 6px 6px 0px 0px;
    background: url(../static/news9_img.png);
    background-position: 50% 50%;
    background-size: cover;
    background-repeat: no-repeat;

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
      color: #666666;
      font-size: 16px;
      line-height: 25px;
    }
  }
  .footer {
    display: grid;
    align-content: center;
    align-items: center;
    color: #b3b3b3;
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
        background-color: rgba(0, 0, 0, 0.05);
        cursor: pointer;
      }
    }
  }
}
</style>
