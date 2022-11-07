<template>
  <section class="contentOne">
    <main>
      {{ text }}
    </main>
  </section>
</template>

<script>
export default {
  name: "MainComp",
  data() {
    return {
      text: "--> Content goes here <--",
    };
  },
};
</script>

<style lang="scss" scoped>
@import '../assets/scss/mixing';
.contentOne {
  background-color: rgb(28, 28, 33);

  main {
    @include container;
    padding: 100px 20px;
    color: white;
    font-size: 20px;
    font-weight: bold;
  }
}
</style>