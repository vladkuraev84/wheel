<template>
  <div class="c-roulette">
    <div class="c-roulette">
      <div class="c-roulette-ar"><img src="../assets/img/roulette-ar.svg" alt="arrow"></div>
      <canvas
          ref="ccanvas"
          width="338"
          height="338"
          :style="{'transform': 'rotate(' + degree + 'deg)'}"
      />
      <span class="number" ref="position">{{ position }}</span>
      <!--          :style="{ 'transform': degree ? 'none' : null }" -->
    </div>
    <br/>
    <br/>
    <button @click="startRoulette">Roll!</button>
  </div>
</template>

<script>
export default {
  name: "roulette",
  data() {
    return {
      position: null,
      random: '',
      degree: 0,
      total: 0,
      timeout: null,
      options: [
          36,
          11,
          30,
          8,
          23,
          10,
          5,
          24,
          16,
          33,
          1,
          20,
          14,
          31,
          9,
          22,
          18,
          29,
          7,
          28,
          12,
          35,
          3,
          26,
          0,
          32,
          15,
          19,
          4,
          21,
          2,
          25,
          17,
          34,
          6,
          27,
          13
      ],
    }
  },
  computed: {

  },

  methods: {
    startRoulette() {
      this.position = '';

      this.random = Math.floor(Math.random() * 36);
      let positionNum = this.options.indexOf(this.random);

      this.degree = Number(360 + (360 - positionNum*10) + 5);

      setInterval(() => {
        this.position = this.random
      }, 7200)

    }
  }
}
</script>