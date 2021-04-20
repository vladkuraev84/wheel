<template>
  <div class="c-keyboard-wr">
    <p class="choice">{{ choice }}</p>
    <div class="c-keyboard">
      <button
        name="19 to 36"
        class="c-btn c-range-1936"
        id="range1936"
        @click="active"
        :data-amount="range1936">
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
        @click="active"
        :data-amount="odd">
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
        @click="active"
        :data-amount="black">
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
        @click="active"
        :data-amount="red">
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
        @click="active"
        :data-amount="even">
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
        @click="active"
        :data-amount="range118">
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
        @click="active"
        :data-amount="range2536">
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
        @click="active"
        :data-amount="range1324">
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
        @click="active"
        :data-amount="range112">
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
        @click="active"
        :data-amount="row1">
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
        @click="active"
        :data-amount="row2">
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
        @click="e => e.target.classList.toggle('active')"
        :data-amount="row3">
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
        @click="active"
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
        items: 37,
        choice: 'Сделайте свой выбор',
        range1936: [19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36],
        odd: [1,3,5,7,9,11,13,15,17,19,21,23,25,27,29,31,33,35],
        black: [2,4,6,8,10,11,13,15,17,20,22,24,26,28,29,31,35],
        red: [1,3,5,7,9,12,14,16,18,19,21,23,25,27,30,32,33,34,36],
        even: [2,4,6,8,10,12,14,16,18,20,22,24,26,28,30,32,34,36],
        range118: [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18],
        range2536: [25,26,27,28,29,30,31,32,33,34,35,36],
        range1324: [13,14,15,16,17,18,19,20,21,22,23,24],
        range112: [1,2,3,4,5,6,7,8,9,10,11,12],
        row1: [3,6,9,12,15,18,21,24,27,30,33,36],
        row2: [2,5,8,11,14,17,20,23,26,29,32,35],
        row3: [1,4,7,10,13,16,19,22,25,28,31,34],
      }
    },
    methods: {
      active(e) {
        this.choice = 'Вы выбрали: ';

        e.target.classList.toggle('active');
        let elements = document.querySelectorAll('.c-btn.active');

        for (let elem of elements) {
          let res = null;
          res = elem.dataset.amount;
          this.choice += res.concat(', ');
        }

        if (elements.length == 0) {
          this.choice = 'Вы ничего не выбрали'
        }
      }
    }
  }
</script>