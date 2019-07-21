<template>
  <div class="a">
    <div class="header">
      <span>
        Last news
      </span>
      <img class="icon"
           src="ic_more_horiz.svg" />
    </div>
    <div class="line" />
    <div class="news">
      <div class="content">
        5 Ways to make your Bbq a memorable family event
      </div>
      <div class="date">
        Yesterday, 7:04 PM
      </div>
    </div>
    <div class="line" />
    <div class="news">
      <div class="content">
        Effective forms advertising internet web site
      </div>
      <div class="date">
        26 Nov, 5:04 PM
      </div>
    </div>
    <div class="line" />
    <div class="news">
      <div class="content">
        Success steps for your personal Or Business Life
      </div>
      <div class="date">
        25 Nov, 5:35 PM
      </div>
    </div>
    <div class="line" />
    <div class="news">
      <div class="content">
        Peace on earth a worderful wish but no way
      </div>
      <div class="date">
        22 Nov, 2:49 AM
      </div>
    </div>
    <div class="line" />
    <div class="footer">
      SHOW MORE
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
.a {
  display: grid;
  height: 600px;

  grid-template-rows: 60px 2px 1fr 2px 1fr 2px 1fr 2px 1fr 2px 60px;
  grid-area: a;
  .header {
    display: flex;
    justify-content: space-between;
    span {
      padding: 0 20px;
      color: #666666;
      font-size: 14px;
      line-height: 60px;
    }
    .icon {
      align-self: center;
      margin-right: 15px;
      &:hover {
        border-radius: 100%;
        background-color: rgba(0, 0, 0, 0.05);
        cursor: pointer;
      }
    }
  }
  .news {
    padding: 20px;
    padding-bottom: 18px;
    .content {
      color: #666666;
      font-size: 14px;
      line-height: 20px;
    }
    .date {
      margin-top: 10px;
      color: #b3b3b3;
      font-size: 12px;
      line-height: 28px;
    }
    &:nth-child(5) {
      background: linear-gradient(180deg, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.5) 98.98%), url(../static/news1_img.png);
			background-position: 50% 50%;
      background-size: cover;
      background-repeat: no-repeat;
      .content {
        color: #f7f7f7;
      }
      .date {
        color: white;
      }
    }
    &:hover {
      background-color: rgba(0, 0, 0, 0.05);
      cursor: pointer;
    }
  }
  .footer {
    align-self: center;
    color: #b3b3b3;
    text-align: center;
    text-transform: uppercase;
    letter-spacing: 1.25px;
    font-weight: 900;
    font-size: 10px;
    line-height: 60px;
    &:hover {
      background-color: rgba(0, 0, 0, 0.05);
      cursor: pointer;
    }
  }
}
</style>
