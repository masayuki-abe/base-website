<template>
  <header class="l-header">
    <h1>
      <a href="/">
        <atomsSiteName />
      </a>
    </h1>
    <atomsTheHumbergerButton
      v-if="isSp"
      :class="{'is-active' : gnaviOn}"
      @btnMenu="toggleMenu"
    />
    <transition name="jsGlobalNavi">
      <organismsTheGlobalNavi
        v-if="gnaviOn || !isSp"
      />
    </transition>
  </header>
</template>

<script>
export default {
  data () {
    return {
      gnaviOn: false,
      wWidth: 768

    }
  },
  computed: {
    isSp () {
      return this.wWidth < 769
    }
  },
  mounted () {
    this.wWidth = window.innerWidth
    console.log(this.wWidth)
    this.$nextTick(() => {
      window.addEventListener('resize', () => {
        this.wWidth = window.innerWidth
      })
    })
  },
  methods: {
    toggleMenu () {
      this.gnaviOn = !this.gnaviOn
    },
    beforeEnter (el) {
      el.style.height = '0'
    },
    enter (el) {
      el.style.height = el.scrollHeight + 'px'
    },
    beforeLeave (el) {
      el.style.height = el.scrollHeight + 'px'
    },
    leave (el) {
      el.style.height = '0'
    }
  }
}
</script>