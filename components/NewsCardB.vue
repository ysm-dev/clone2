<template>
  <div class="b">
    <div class="header">
      <img class="label"
           src="label_food.svg" />
      <div class="content">
        Peace On Earth A Wonderful Wish But No Way
      </div>
      <img class="button"
           src="button_circle.svg" />
    </div>
    <div class="line" />
    <div class="footer">
      <span class="date">
        24 Jun, 5:40 PM
      </span>
      <div class="center">
        <div class="view">
          <img src="ic_remove_red_eye.svg"
               alt=""
               class="icon">
          <span class="count">
            275
          </span>
        </div>
        <div class="comments">
          <img src="ic_forum.svg"
               class="icon">
          <span class="count">
            15
          </span>
        </div>
      </div>
      <span class="author">
        Andre McBride
      </span>
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
.b {
  position: relative;
  display: grid;
  height: 330px;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.3) 0%, rgba(0, 0, 0, 0.5) 100%), url('../static/news2_img.png');
  background-size: cover;
  background-position: 50% 50%;
  background-repeat: no-repeat;

  grid-template-rows: 1fr 2px 60px;
  grid-area: b;
  .header {
    display: flex;
    align-items: center;
    flex-direction: column;
    .label {
      margin-top: 60px;
    }
    .content {
      margin-top: 35px;
      width: 325px;
      color: white;
      text-align: center;
      font-size: 24px;
      line-height: 40px;
    }
    .button {
      position: absolute;
      top: 30px;
      right: 30px;
      &:hover {
        border-radius: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        cursor: pointer;
      }
    }
  }
  .footer {
    display: grid;
    align-content: center;
    align-items: center;
    color: white;
    font-size: 13px;
    line-height: 60px;

    grid-auto-flow: column;
    .date {
      justify-self: start;
      margin-left: 30px;
    }
    .center {
      display: flex;
      justify-self: center;
      .view {
        display: flex;
        padding: 0 16px;
        .icon {
          margin-right: 8px;
        }
        .count {
          font-size: 12px;
        }
        &:hover {
          background-color: rgba(0, 0, 0, 0.5);
          cursor: pointer;
        }
      }
      .comments {
        padding: 0 16px;
        display: flex;
        justify-self: center;
        .icon {
          margin-right: 8px;
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
    .author {
      margin-right: 25px;
      justify-self: end;
    }
    /* &:hover {
      background-color: rgba(0, 0, 0, 0.05);
      cursor: pointer;
    } */
  }
}
</style>
