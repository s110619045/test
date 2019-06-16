<template>
  <div class="container-grid">
    <Nav/>
    <!-- <Gallery :totalNews = 'totalNews' />
    <SelectedNews :selectedNews = 'selectedNews' />   -->
    <ShopPageTop/>
    <Section />
    <Footer />
  </div>
</template>

<script>
import { mapActions } from 'vuex';
import { mapGetters } from 'vuex';

import Nav from "../components/Nav";
import ShopPageTop from "../components/ShopPageTop";
// import ShopList from "../components/ShopList";

// import Footer from "../components/Footer";

export default {
  name: "Main",
  components: {
    Nav,
    // ShopList,
    ShopPageTop
    // Footer
  },
  computed: mapGetters(['totalNews', 'selectedNews']),
  methods: mapActions(['init']),
  created() {
    this.init();
  }
};
</script>

<style lang="postcss">
@import "../styles/base/_variables.css";
@import "../styles/base/_global.css";
</style>

