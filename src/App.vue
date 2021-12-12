<template>
  <div className="flex justify-center items-center bg-blue-400 h-screen w-full">
    <img
      className="w-1/2"
      :src="require(`./assets/images/${imageSrc}.png`)"
      alt="Ball"
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
      this.imageSrc = ballList[Math.floor(Math.random() * ballList.length)]
    },
  },
}
</script>
