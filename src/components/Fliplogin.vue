<template>
    <div class="flip-container"
       :class="{ 'flipit': flipit }"
       :style="{ width: width, height: height }"
       >
    <div class="flipper cardStyle">
      <div class="front cardStyle">
        <slot name="front">
          </slot>
      </div>
      <div class="back cardStyle">
        <slot name="back">
        </slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    'width': {
      type: String,
      required: true
    },
    'height': String,
    'flipit': {
      type: Boolean,
      required: true,
      default: false
    }
  },
  data () {
    return {
    }
  }
}
</script>

<style>
.cardStyle {
    height: 50%;
    width : 100%;
    transition : '0.5s';
}
 .flip-container {
    perspective: 1000;
  }
  .flip-container.flipit .flipper,
  .flip-container.hover .flipper {
    transform: rotateY(180deg);
  }
  .flipper {
    transition: 0.6s;
    transform-style: preserve-3d;
    position: relative;
  }
  .front, .back {
    backface-visibility: hidden;
    position: absolute;
    top: 0;
    left: 0;
  }
  .front {
    z-index: 2;
    -webkit-transform: rotateY(0);
    -moz-transform: rotateY(0);
    -o-transform: rotateY(0);
    transform: rotateY(0);
  }
  .back {
    -webkit-transform: rotateY(180deg);
    -moz-transform: rotateY(180deg);
    -o-transform: rotateY(180deg);
    transform: rotateY(180deg);
  }
</style>
