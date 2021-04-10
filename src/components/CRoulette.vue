<template>
  <div class="c-roulette">
    <div class="c-roulette">
      <div class="c-roulette-ar"><img src="../assets/img/roulette-ar.svg" alt="arrow"></div>
      <canvas id="ccanvas" width="338" height="338" />
    </div>
    <button @click="startRoulette">Roll!</button>
  </div>
</template>

<script>
export default {
  name: "roulette",
  data() {
    return {
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

  methods: {
    startRoulette() {
      let random = Math.floor(Math.random() * 36);
      console.log(random)
    }
  }
}
</script>