<template>
  <div class="flex justify-center items-center bg-blue-400 h-screen w-full">
    <img
      class="w-1/2"
      :src="require(`./assets/images/${imageSrc}.png`)"
      :alt="imageSrc"
      @click="ballChange"
    />
  </div>
</template>

<script>
export default {
  name: 'App',

  data: () => ({
    imageSrc: 'ball1',
  }),

  methods: {
    ballChange() {
      const ballList = ['ball1', 'ball2', 'ball3', 'ball4', 'ball5']

      const randomIndex = Math.floor(Math.random() * ballList.length)

      if (ballList[randomIndex] === this.imageSrc) {
        this.ballChange()
      } else {
        this.imageSrc = ballList[randomIndex]
      }
    },
  },
}
</script>
