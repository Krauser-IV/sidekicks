
<template>
  <div class="banner_bar">
    <div v-if="direction == 'left'" class="wrapper slide_left">
      <p v-for="i in count" :key="i">Coming Soon</p>
    </div>
    <div v-else class="wrapper slide_right">
      <p v-for="i in count" :key="i">Coming Soon</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 80,
    };
  },
  props: {
    direction: String,
  },
};
</script>

<style lang="scss">
.banner_bar {
  width: 100vw;
  overflow: hidden;
  background: var(--primaryColor);
  padding: 5px 0px;
  height: 6%;
  display: flex;
  align-items: center;
  .wrapper {
    width: auto;
    display: flex;
    gap: 5px;
    animation-duration: 160s;
    animation-iteration-count: infinite;
    animation-direction: alternate;
    animation-timing-function: linear;
    p {
      padding: 5px 5px;
      text-transform: uppercase;
      color: white;
      position: relative;
      font-size: 1.3rem;
      margin-right: 10px;
      white-space: nowrap;
      font-weight: 900;
      &::after {
        content: "";
        width: 5px;
        height: 5px;
        border-radius: 50%;
        background: white;
        position: absolute;
        left: -8px;
        top: 50%;
        transform: translateY(-50%);
      }
    }
  }
  .slide_left {
    animation-name: slideLeft;
  }
  .slide_right {
    animation-name: slideRight;
  }
}
@media only screen and (max-width: 600px) {
  .wrapper {
    width: 1200% !important;
  }
}
@keyframes slideRight {
  from {
    transform: translateX(0%);
  }
  to {
    transform: translateX(-30%);
  }
}
@keyframes slideLeft {
  from {
    transform: translateX(-30%);
  }
  to {
    transform: translateX(0%);
  }
}
</style>
