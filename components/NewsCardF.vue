<template>
  <div class="f">
    <img src="label_food.svg"
         class="label">
    <div class="count">
      1,256
    </div>
    <div class="content">
      The Basics Of Western Astrology Explained
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.f {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 240px;
  background-color: #1875f0 !important;
  color: white;

  grid-template-rows: 90px 1fr 2px 60px;
  grid-area: f;
  .label {
    position: absolute;
    top: 35px;

    align-self: center;
  }
  .count {
    margin-top: 5px;
    text-align: center;
    font-size: 48px;
    line-height: 90px;
  }
  .content {
    align-self: center;
    width: 150px;
    text-align: center;
    font-size: 14px;
    line-height: 20px;
  }
}
</style>
