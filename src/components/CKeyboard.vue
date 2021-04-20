<template>
  <div class="c-keyboard-wr">
    <div class="c-keyboard">
      <button
        name="19 to 36"
        class="c-btn c-range-1936"
        id="range1936"
        data-amount="">
          <span class="">
            <span class="">19 to 36</span>
          </span>
          <span class="c-rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="odd"
        class="c-btn c-odd"
        id="odd"
        data-amount="">
          <span class="">
            <span class="">Odd</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="black"
        class="c-btn c-black"
        id="black"
        data-amount="">
          <span class="">
            <span class="">Black</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="red"
        class="c-btn c-red"
        id="red"
        data-amount="">
          <span class="">
            <span class="">Red</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="even"
        class="c-btn c-even"
        id="even"
        data-amount="">
          <span class="">
            <span class="">Even</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="1 to 18"
        class="c-btn c-range-118"
        id="range118"
        data-amount="">
          <span class="">
            <span class="">1 to 18</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="25 to 36"
        class="c-btn c-range-2536"
        id="range2536"
        data-amount="">
          <span class="">
            <span class="">25 to 36</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="13 to 24"
        class="c-btn c-range-1324"
        id="range1324"
        data-amount="">
          <span class="">
            <span class="">13 to 24</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="1 to 12"
        class="c-btn c-range-112"
        id="range112"
        data-amount="">
          <span class="">
            <span class="">1 to 12</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="1:1"
        class="c-btn c-row1"
        id="row1"
        data-amount="">
          <span class="">
            <span class="">1:1</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="2:1"
        class="c-btn c-row2"
        id="row2"
        data-amount="">
          <span class="">
            <span class="">2:1</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        name="3:1"
        class="c-btn c-row3"
        id="row3"
        data-amount="">
          <span class="">
            <span class="">3:1</span>
          </span>
          <span class="rate">
            <span class=""></span>
          </span>
      </button>
      <button
        v-for="(item, index) in items" :key="item"
        :name="`simple-${index}`"
        :class="`color-simple c-btn number-${index}`"
        :id="`colorSimple-${index}`"
        :data-amount="`${index}`"
      >
          <span class="">
            <span class="">{{ index }}</span>
          </span>
          <span class="">
            <span class=""></span>
          </span>
      </button>
    </div>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        items: 37
      }
    },
  }
</script>