<template>
  <div class="main">
    <Jumbotron/>
    <ListMatches/>
  </div>
</template>

<script>
import Jumbotron from "@/components/Jumbotron.vue";
import ListMatches from "@/components/ListMatches.vue";

export default {
  components: {
    Jumbotron,
    ListMatches
  }
};
</script>

<style lang="scss" scoped>
.main {
  margin: 25px;
}
</style>
