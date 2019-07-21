<template>
  <div class="k">
    <img src="label_ad.svg" />
    <div class="button">
      <span>
        visit site
      </span>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.k {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background: url(../static/news11_img.png);
  background-position: 50% 50%;
  background-size: cover;
  background-repeat: no-repeat;
  color: white;

  grid-area: k;
  img {
    margin-top: 35px;
  }
  .button {
    display: flex;
    align-self: center;
    justify-content: center;
    margin-bottom: 60px;
    width: 120px;
    height: 40px;
    border-radius: 30px;
    background: rgba(0, 0, 0, 0.3);
    span {
      color: #ffffff;
      text-align: center;
      text-transform: uppercase;
      letter-spacing: 1.25px;
      font-weight: 900;
      font-size: 10px;
      line-height: 40px;
      opacity: 1;
    }
    &:hover {
      background-color: rgba(0, 0, 0, 0.5);
      cursor: pointer;
    }
  }
}
</style>
