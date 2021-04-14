<template>
  <HeaderComponent/>
  <Hinweis/>
  
  <!--
  <div id="nav">
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/create-parent">Create new Parent</router-link></li>
      <li><router-link to="/create-child">Create new Child</router-link></li>
    </ul>
  </div>
  -->

  <router-view/>

  <FooterComponent/>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import Hinweis from "./components/Hinweis.vue";
import FooterComponent from "./components/FooterComponent.vue";
export default {
  name: "App",
  components: {
    HeaderComponent: HeaderComponent,
    Hinweis: Hinweis,
    FooterComponent: FooterComponent
  },
  beforeCreate() {
    this.$store.commit('initializeStore');
  }
};
</script>