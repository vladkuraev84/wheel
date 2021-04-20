<template>
  <div class="c-roulette">
    <div class="c-roulette">
      <div class="c-roulette-ar"><img src="../assets/img/roulette-ar.svg" alt="arrow"></div>
      <canvas ref="ccanvas" width="338" height="338" :style="{ 'transform': degree ? 'none' : null }" />
    </div>
    <button @click="startRoulette">Roll!</button>
  </div>
</template>

<script>
export default {
  name: "roulette",
  data() {
    return {
      degree: null,
      timeout: null,
      options: [
          '36',
          '11',
          '30',
          '8',
          '23',
          '10',
          '5',
          '24',
          '16',
          '33',
          '1',
          '20',
          '14',
          '31',
          '9',
          '22',
          '18',
          '29',
          '7',
          '28',
          '12',
          '35',
          '3',
          '26',
          '0',
          '32',
          '15',
          '19',
          '4',
          '21',
          '2',
          '25',
          '17',
          '34',
          '6',
          '27',
          '13'
      ],
    }
  },
  computed: {

  },

  methods: {
    startRoulette() {
      console.log(this.$refs.ccanvas);

      let random = Math.floor(Math.random() * 36);
      // this.$refs.ccanvas.style.transform = 'rotate(360deg)';
      console.log(random);
      this.timeout = setInterval(() => {
        this.$refs.ccanvas.style.transform = 'rotate(360deg)';
      }, 1)

    }
  }
}
</script>