<template>
  <div class="carousel">
    <div class="inner">
      <div class="images" @click="next">
        <div class="img_list" ref="imgList">
          <div class="img_item" v-for="(item, i) in items" :key="i + 'imgItem'">
            <img :src="item" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      default: [],
    },
  },
  data() {
    return {
      index: 0,
      length: 3,
    };
  },
  watch: {
    items: {
      handler: function (value) {
        this.length = value ? value.length : -1;
        this.reset();
      }
    },
  },
  methods: {
    clickDot(index) {
      this.index = index;
      this.changeImg();
    },
    next() {
      this.index = this.index + 1;
      this.changeImg();
    },
    changeImg() {
      console.log(123)
      const percent = -100 * this.index;
      this.$refs.imgList.style.transform = `translateX(${percent}%)`;
    },
    reset() {
      this.$refs.imgList.style.transform = 'translateX(0)';
      console.log(this.$refs.imgList.style.transform)
      this.index = 0;
    },
  },
};
</script>

<style lang="scss" scoped>
.carousel {
  position: relative;
  width: 100%;
  background: #c3c3c3;
  height: 570px;
  overflow: hidden;
  .images {
    overflow: hidden;
    &::after {
      content: "";
      display: block;
      padding-bottom: 135%;
    }
    .img_list {
          display: flex;
    align-items: center;
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      display: flex;
      flex-wrap: nowrap;
      transition: transform 1s;
      .img_item {
        flex: 0 0 100%;
      }
    }
  }
}
</style>