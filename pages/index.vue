<template>
  <div class="container">
    <div class="frame">
      <div class="statusbar"
           :style="{
        background: isOpen ? '#f5f5f5' : 'white'
        }">
        <span class="time">
          {{ `${new Date().getHours() % 12}:${new Date().getMinutes().length === 1 ? `0${new Date().getMinutes()}` : new Date().getMinutes()}` }}
        </span>
        <img class="icons"
             src="statusbar_icons.svg" />
      </div>
      <div class="nav">
        <img class="left__arrow"
             src="left_arrow.svg" />
        <span class="title">
          Categories
        </span>
      </div>
      <div class="items__scroll">
        <div class="item__list">
          <div class="item"
               v-for="(item,i) in items"
               :key="i"
               @click="isOpen = !isOpen">
            <div class="image"
                 :style="{
                backgroundImage: `url(${item.img})`
                }" />
            <span class="title">{{ item.title }}</span>
            <span class="count">{{ item.count }} items</span>
            <img class="right__arrow"
                 src="right_arrow.svg" />
          </div>
        </div>
      </div>
      <transition name="slide">
        <div v-show="isOpen"
             class="collection">
          <div class="hero">
            <div class="cover"
                 :style="{
                backgroundImage: `url('cover.png')`
                }" />
            <span class="subtitle">
              Cyber Monday
            </span>
            <span class="title">
              Sale Up To 70% Off
            </span>
          </div>
          <img class="close"
               src="close.svg"
               @click="isOpen = !isOpen" />
          <div class="shop">
            <img src="shop.svg" />
          </div>
          <div class="test">
            허허
          </div>
        </div>
      </transition>
    </div>
    <img class="wireframe"
         src="wireframe.png" />
  </div>
</template>

<script>
const data = [
  {
    img:
      'https://s3-alpha-sig.figma.com/img/8218/5f10/82c74bbab21568b3d2fb61d984187770?Expires=1564358400&Signature=BHqyn5zIJ2SSFE~ZT2doyQ33WZ9QFie1bXi3ExmU5md2MbSzGgdkf9SB~hMbpJ86FamJBfq6TpJ4mqerErg~xb2OGzGAJDfToo8x68UgFHqIwBzllKwmIjPrYb2jwJ-~xEpikE1pbTPFpPCkQ6hVG8nJBDpUai~Pq5qXBVLptb3qUqtriIZHq20WRJKOzojF~K3WwBdK6CVRxfrsXbolBFGt--KAn09FDGdAsMxOehnGgRRvMda260Hx2ZXClhMuG0YMW~zpNPjMLA5hu4QCcGtpGXRGVh7trnaOouMpeKcijPZFGQjwl~7-npR4uWPK2tWbxhCCOgiQgh4NvunyEQ__&Key-Pair-Id=APKAINTVSUGEWH5XD5UA',
    title: 'Decoration',
    count: 1065,
  },
  {
    img:
      'https://s3-alpha-sig.figma.com/img/4d1c/8463/0fd91c8aa27859f5acac547eda0d1073?Expires=1564358400&Signature=dXIXyHsb2XTOGwuQMzs~KKKszV60Bm5SsimLk2MaQZTcFP1SamhzN2yajoQf69ryCw61yyj0Yv9HgQ5jB~FZE7mZz5XZIwXz66zf-d75JL6o9JCuP9xuLM7RTVz~Y4wMA90QwyVBmO2J41K1MQ-X-WSdhl2QfGpSDtsxj9IDpGIf~2MJqhiBLp34x1fDYWgEzgBk5zOT424l3xt2CvMt1OERBsyxre2ye8AvOPwvkhQEXiv6IEhy57jUAE-UXujXIXNXqVYPpAKcF9acFf8XznUh0DJtgqgXdfmtwaUJtEqvIJYqkKHU5ZCSIOFxPsDmBsZ-489be07nMAehbkbX-g__&Key-Pair-Id=APKAINTVSUGEWH5XD5UA',
    title: 'Ceiling',
    count: 827,
  },
  {
    img:
      'https://s3-alpha-sig.figma.com/img/ad83/b334/8429685214169c5c13c3041c8544b6e1?Expires=1564358400&Signature=JWaXFVt4gXVuRwVuo0dKjmBZMXgCr3CjKEOlE37BESumSLtrabawy48B9Pf5ulvhog5Hb0Xdxps~KJbgTlEUj1J9eUb0dJ~IoFTEme5g4I3y-DlLWOSmHd3fixgFuyV9BWanmsequVGK7xS~eDxgMoMFPJq-X~o42aY84z5S7mVFRw-R8qrG5odXGczVFx8bnLWvJl6nadWGbs~2PGIFSXm5VpjeTngz8UP7QzV667Eep9VUF9jlRnM64LvkXH3RpGmQtG~GEN9IqohQZdjpCOdvSN1ioL14eutgZRnZUbmHQIt97JxKO5AfBO~5Jy4IF~6JLF9niR-uIgSQs3AMmA__&Key-Pair-Id=APKAINTVSUGEWH5XD5UA',
    title: 'Floor',
    count: 1423,
  },
  {
    img:
      'https://s3-alpha-sig.figma.com/img/42ef/2011/a410f00d8e5c8c573ab19b2ce7befddb?Expires=1564358400&Signature=X6XWXoveQPH0ZOQwGuCHbXRNKmYEhPyra0iLZQ8mbalsL-USi~UtiDaY38qSNn71nY2n5YVvDJmNv6gDxtzI5r~F4niLMLaRaV0pqh7cKMOFCLoxSdjCIKxEKnt73s4YW6BBQj7xkIFDYXVpKu~Kai8jODxRSBBXBEBKp0IN9wLhAq7D6avkKvx6~3QqP1EhXBVkzBoMNU~vpxpCEgMrwxxkJ~wDIUkp-gNRnSToYLRCured79KqyDYA6qdqV14lqbVNvjUGWDd~0hfc7ym4PEabzO6yntwxOzASkoIzADtXajhHkeBps9JwzHtAPNUcAwXpFmxVQbvxC7JuQofpVg__&Key-Pair-Id=APKAINTVSUGEWH5XD5UA',
    title: 'Furniture',
    count: 4126,
  },
  {
    img:
      'https://s3-alpha-sig.figma.com/img/0d62/03ae/4b2fdb7ba7684b05447f724fbc60bd7a?Expires=1564358400&Signature=VJI34DquScBFZjXquliouFSeTP5qcOxTyV4ftZ1syofMG96TomH5hT55HQ0WEpSiE6c-wLgefTroHgtRivu~vrPQXciKABonJNqgp4BQEyOPvcDmeKI6yR~dGBbjeAuDH~72imNlZm7CtnXV2KxGtWLVN70Q-6ZGCU7zOjtTjw6zMQpOEC~QK6RqaKP2ckpLodsTy7mihEMn1SjHQkCi3~P8CHD8xZHCFWPchaNoEcYBzXCDaObdme3HwFrQhtLONhoYDrjmNSB1cEwY4ehf8NGRxGk9Oa5uiddmG1NrSsrZxXfVYUHkTHLGvvDY1XZDdERsoEV-1EPRwXuutYY1aQ__&Key-Pair-Id=APKAINTVSUGEWH5XD5UA',
    title: 'Lamps',
    count: 1126,
  },
  {
    img:
      'https://s3-alpha-sig.figma.com/img/397f/9c95/3a81502c61272fcaddbd4d3a41bddd0e?Expires=1564358400&Signature=Kuu8eZx4ZVoxGHJzJVecvgbXiI5fGxNCk88oSuh4vIAvJEWQSZcidmzBJnnJZ4nikniQExKPiXu7-oQ4hQ6k5kd2S79uFfGkHZZJBwGFaHbKx4C5w2LWxG2dQqhpz1oVkZZTSQEPs7gVYWBecCGSmn4wG5bT6xosE30L2G6yW4GeBDg65G9XuMrW~piQeBdc-9Juz2Z0ImS-fzf5Vwj8MEssX7TNbamHJF88WQRDALH7dGR7w6w6dqIw0C1pDNxhJl0PdE4H41ZpKu-XFreoEpns1FWbjaqFWf3qy5aCAZfHwrwdS3d-u56shzJBEYRTc8KKetgQHcrrzMCcnrKCiw__&Key-Pair-Id=APKAINTVSUGEWH5XD5UA',
    title: 'Wooden',
    count: 1126,
  },
]
export default {
  data() {
    return {
      items: [...data, ...data],
      isOpen: true,
    }
  },
  components: {},
}
</script>

<style lang="scss" scoped>
@keyframes slideUp {
  from {
    transform: translateY(100%);
  }
  to {
    transform: translateY(0%);
  }
}

@keyframes slideDown {
  from {
    transform: translateY(0%);
  }
  to {
    transform: translateY(100%);
  }
}

$duration: 0.3s;
$ease: cubic-bezier(0, 0, 0.2, 1);
$overshoot: cubic-bezier(0.175, 0.885, 0.32, 1.275);

.slide-enter-active {
  animation: slideUp $duration $ease;
}

.slide-leave-active {
  animation: slideDown $duration $ease;
}

.container {
  display: grid;
  position: relative;
  height: 100%;
  background: #f2f2f2;
  .frame {
    position: relative;
    justify-self: center;
    display: grid;
    width: 375px;
    height: 813px;
    align-self: center;
    background: white;
    overflow: hidden;
    .statusbar {
      position: fixed;
      width: 375px;
      height: 44px;
      background: #ffffff;
      z-index: 1;
      transition: all $duration;
      .time {
        position: absolute;
        top: 0;
        bottom: 0;
        margin: auto;
        font-family: 'SF Pro Text';
        font-style: normal;
        font-weight: 600;
        font-size: 15px;
        line-height: 18px;
        text-align: center;
        letter-spacing: -0.165px;
        width: 54px;
        height: 18px;
        left: 19.89px;
        color: #000000;
      }
      .icons {
        position: absolute;
        top: 0;
        bottom: 0;
        margin: auto;
        right: 14.5px;
      }
    }
    .nav {
      margin-top: 43px;
      height: 44px;
      width: 375px;
      position: fixed;
      background: #ffffff;
      box-shadow: 0px 0.5px 0px rgba(0, 0, 0, 0.1);
      display: grid;
      .left__arrow {
        position: absolute;
        left: 15px;
        align-self: center;
        cursor: pointer;
        &:hover {
          background-color: rgba(0, 0, 0, 0.1);
          border-radius: 100px;
        }
      }
      .title {
        font-family: 'Avenir';
        font-style: normal;
        justify-self: center;
        align-self: center;
        font-weight: 800;
        font-size: 17px;
        line-height: 22px;
        text-align: center;
        letter-spacing: -0.41px;
        position: absolute;
        height: 22px;
      }
    }
    .items__scroll {
      overflow: scroll;
      margin-top: 88px;
      width: 375px;
      height: 741px;
      background: white;
      border-radius: 0px 0px 20px 20px;
      .item__list {
        display: flex;
        flex-direction: column;
        .item {
          position: relative;
          height: 119px;
          border-bottom: 1px solid rgba(0, 0, 0, 0.2);
          cursor: pointer;
          &:hover {
            background-color: rgba(0, 0, 0, 0.05);
          }
          .image {
            position: absolute;
            top: 0;
            bottom: 0;
            left: 15px;
            margin: auto;
            border-radius: 8px;

            width: 88px;
            height: 88px;
            background-position: center;
            background-size: cover;
          }
          .title {
            font-family: Avenir;
            font-style: normal;
            font-weight: 800;
            font-size: 17px;
            line-height: 22px;
            letter-spacing: -0.41px;
            width: 200px;
            position: absolute;
            top: 28px;
            left: 118px;
          }
          .count {
            font-family: Avenir;
            font-style: normal;
            font-weight: normal;
            font-size: 15px;
            line-height: 20px;
            letter-spacing: -0.24px;
            color: rgba(0, 0, 0, 0.4);
            position: absolute;
            bottom: 39px;
            left: 118px;
          }
          .right__arrow {
            position: absolute;
            margin: auto;
            top: 0;
            bottom: 0;
            right: 15px;
          }
        }
      }
    }
    .collection {
      position: absolute;
      width: 375px;
      height: 900px;
      overflow: scroll;
      .hero {
        margin-top: -120px;
        .cover {
          background-position: center;
          background-size: cover;
          height: 643px;
        }
        .subtitle {
          font-family: Avenir;
          font-style: normal;
          font-weight: normal;
          font-size: 17px;
          line-height: 20px;
          letter-spacing: -0.272px;
          color: rgba(0, 0, 0, 0.4);
          position: absolute;
          left: 30px;
          top: 419px;
        }
        .title {
          font-family: Poppins;
          font-style: normal;
          font-weight: 600;
          font-size: 40px;
          line-height: 44px;
          letter-spacing: 0.482353px;
          color: #000000;
          position: absolute;
          left: 30px;
          top: 442px;
        }
      }
      .close {
        position: absolute;
        top: 52px;
        left: 8px;
        z-index: 1;
        cursor: pointer;
        &:hover {
          background-color: rgba(0, 0, 0, 0.05);
        }
      }
      .shop {
        height: 81px;
        background: #f5f5f5;
        position: relative;
        img {
          position: absolute;
          top: 0;
          bottom: 0;
          left: 30px;
          margin: auto;
        }
      }
      .test {
        background: white;
        height: 800px;
      }
    }
  }
  .wireframe {
    pointer-events: none;
    position: absolute;
    justify-self: center;
    align-self: center;
    margin-top: 31px;
    margin-right: 4px;
    z-index: 2;
  }
}
</style>
