<template>
  <ul>
    <li
      v-for='(item, key) of cities'
      :key='key'
      :ref='key'
      @click='handleClick'
      @touchstart='handleTouchStart'
      @touchmove='handleTouchMove'
      @touchend='handleTouchEnd'
    >
      {{key}}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  data () {
    return {
      touchStatus: false,
      startY: 0,
      timer: null
    }
  },
  props: {
    cities: Object
  },
  computed: {
    letters () {
      const letters = []
      for (var i in this.cities) {
        letters.push(i)
      }
      return letters
    }
  },
  updated () {
    this.startY = this.$refs['A'][0].offsetTop
  },
  methods: {
    handleClick (e) {
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart (touchStatus) {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.touchStatus) {
        if (this.timer) {
          clearTimeout(this.timer)
        }
        this.timer = setTimeout(() => {
          const clientY = e.touches[0].clientY - 88
          const index = Math.floor((clientY - this.startY) / 14)
          if (index >= 0 && index < this.letters.length) {
            this.$emit('change', this.letters[index])
          }
        }, 16)
      }
    },
    handleTouchEnd (touchStatus) {
      this.touchStatus = false
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/varivles.styl'
  ul
    position: absolute
    z-index: 2
    top: 85px
    right: 0
    bottom: 0
    width: 20px
    text-align: center
    display: flex
    flex-direction: column
    justify-content: center
    li
      margin-top: 2px
      color: $bgColor
</style>
