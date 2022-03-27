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
      <!-- <ul class="dots">
        <li
          class="dot"
          v-for="i in length"
          :key="i + 'dot'"
          :class="{ active: i - 1 === index }"
          @click="clickDot(i - 1)"
        ></li>
      </ul> -->
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
  .images {
    //overflow: hidden;
    &::after {
      content: "";
      display: block;
      padding-bottom: 80%;
    }
    .img_list {
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
  .dots {
    bottom: 0;
    display: flex;
    justify-content: center;
    padding: 15px 0;
    .dot {
      width: 10px;
      height: 10px;
      border-radius: 100%;
      background: #dadada;
      margin: 0 5px;
      cursor: pointer;
      &.active {
        background: var(--text-sub-color);
      }
    }
  }
}
</style>