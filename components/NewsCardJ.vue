<template>
  <div class="j">
    <div class="header">
      <span>
        What people say
      </span>
      <button>
        create theme
      </button>
    </div>
    <div class="line" />
    <div class="content">
      <div class="review"
           v-for="{ img, date, desc } in reviews"
           :key="desc">
        <img :src="img || `face_empty.svg`" />
        <span class="date">{{ date }}</span>
        <span class="desc">{{ desc }}</span>
      </div>
    </div>
    <div class="line" />
    <div class="footer">
      SHOW MORE
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviews: [
        {
          img: 'face1.png',
          date: '24 Jun, 5:40 PM',
          desc: 'Company Logo Design?',
        },
        {
          img: 'face2.png',
          date: '23 Jun, 5:40 PM',
          desc: 'The Amazing Hubble',
        },
        {
          img: 'face3.png',
          date: '12 Jun, 5:40 PM',
          desc: 'Truck Side Advertising Isn...',
        },
        {
          img: 'face4.png',
          date: '9 Jun, 3:40 PM',
          desc: 'Space The Final Frontier',
        },
        {
          img: null,
          date: '4 Jun, 7:40 PM',
          desc: 'Decorate For Less With...',
        },
        {
          img: 'face5.png',
          date: '2 Jun, 8:40 PM',
          desc: 'Look Up In The Sky',
        },
        {
          img: 'face6.png',
          date: '1 Jun, 3:40 PM',
          desc: 'Deciphering Marketing ...',
        },
        {
          img: 'face7.png',
          date: '28 May, 2:40 PM',
          desc: 'What Is The Big R For...',
        },
        {
          img: null,
          date: '27 May, 1:30 PM',
          desc: 'Cooking On A George ...',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.line {
  background-color: #f5f5f5;
}
.j {
  display: grid;
  height: 420px;

  grid-template-rows: 88px 2px 1fr 2px 60px;
  grid-area: j;
  .header {
    display: flex;
    justify-content: space-between;
    span {
      margin-left: 30px;
      color: #666666;
      font-size: 16px;
      line-height: 90px;
    }
    button {
      align-self: center;
      margin-right: 25px;
      width: 130px;
      height: 40px;
      border: 2px solid #f5f5f5;
      border-radius: 4px;
      background: #ffffff;
      color: #b3b3b3;
      text-transform: uppercase;
      letter-spacing: 1.25px;
      font-weight: 900;
      font-size: 10px;
      line-height: 40px;
      &:hover {
        background-color: rgba(0, 0, 0, 0.05);
        cursor: pointer;
      }
    }
  }
  .content {
    display: grid;
    padding: 15px 15px 13px 15px;

    grid-template-columns: 1fr 1fr 1fr;
    .review {
      position: relative;
      display: flex;
      flex-direction: column;
      padding: 15px;
      img {
        position: absolute;
        width: 50px;
        height: 50px;
        border-radius: 100px;
      }
      .date {
        margin-left: 65px;
        color: #b3b3b3;
        font-size: 12px;
        line-height: 25px;
      }
      .desc {
        margin-left: 65px;
        color: #666666;
        font-size: 13px;
        line-height: 25px;
      }
      &:hover {
        border-radius: 4px;
        background-color: rgba(0, 0, 0, 0.05);
        cursor: pointer;
      }
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
