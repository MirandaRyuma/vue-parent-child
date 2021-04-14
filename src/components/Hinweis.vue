<template>
  <footer class="mt-2">
    <p>{{ setText }} <br> {{ selectedParent }}</p>
  </footer>         
</template>

<script>
export default {
  name: "Hinweis",
  props: {
      text: String
  },
  computed: {
    setText() {
        let ausgabe = this.text ? this.text : "Ich bin nur eine Komponente. Hier gibt es sonst nichts zu sehen.";
        return ausgabe;
    },
    selectedParent() {
        return "ID des aussgewählten Parents: " + this.$store.state.selectedParentId;
    }
  } 
};
</script>

<style scoped>
p {
  background-color: yellow;
  color: black;
  padding: 0.2em 0.5em
}
</style>