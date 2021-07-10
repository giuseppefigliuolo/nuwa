<template>
  <p class="mb-0" v-if="compact" :style="{ 'font-size': fontSize }">
    {{ countdownDateShort }}
  </p>
  <p v-else :style="{ 'font-size': fontSize }">
    {{ countdownDate }}
  </p>
</template>

<script>
export default {
  props: {
    fontSize: {
      type: String,
      default: '2.7rem'
    },
    compact: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      countdownDate: '',
      countdownDateShort: '',
      endDate: new Date('Oct 25, 2021 16:37:52').getTime()
    }
  },
  watch: {
    countdownDate: {
      handler(value) {
        if (value >= 0) {
          setInterval(() => {
            const now = new Date().getTime()
            // debugger
            const countdownDateNotFormatted = this.endDate - now
            const days = Math.floor(
              countdownDateNotFormatted / (1000 * 60 * 60 * 24)
            )
            const hours = Math.floor(
              (countdownDateNotFormatted % (1000 * 60 * 60 * 24)) /
                (1000 * 60 * 60)
            )
            const minutes = Math.floor(
              (countdownDateNotFormatted % (1000 * 60 * 60)) / (1000 * 60)
            )
            const seconds = Math.floor(
              (countdownDateNotFormatted % (1000 * 60)) / 1000
            )

            this.countdownDate = `${days}giorni ${hours}ore ${minutes}minuti ${seconds}secondi`
            this.countdownDateShort = `${days}d ${hours}h ${minutes}m ${seconds}s`
          }, 1000)
        }
      },
      immediate: true // This ensures the watcher is triggered upon creation
    }
  }
}
</script>

<style lang="scss" scoped>
p {
  font-family: 'obviously-wide', sans-serif !important;
}
</style>
