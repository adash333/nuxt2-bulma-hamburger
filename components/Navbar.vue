<template>
  <nav class="navbar is-white" >
    <div class="navbar-brand">
      <div class="navbar-item">Nuxt Bulma Hamburger</div>
      <div class="navbar-burger" data-target="navMenu" @click="$store.commit('toggleMenu')" :class="{'is-active': $store.state.isMenuActive}">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div><!-- navbar-brand END -->
    <div class="navbar-menu" :class="{'is-active': $store.state.isMenuActive}">
      <div class="navbar-end">
        <nuxt-link to="/" class="navbar-item">トップ</nuxt-link>
        <nuxt-link to="/about" class="navbar-item">NBHとは？</nuxt-link>
        <nuxt-link to="/contact" class="navbar-item">お問い合わせ</nuxt-link>
      </div>
    </div><!-- navbar-menu END -->
  </nav>
</template>

<script>
export default {
  data: () => {
    return {isMenuActive: false}
  },
  methods: {
    toggleMenu () {
      this.isMenuActive = !this.isMenuActive
    }
  }
}
</script>