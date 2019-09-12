<template>
  <div id="main">
    <h1>Matches</h1>

    <div class="cards-list">
      <CardMatch/>
    </div>
  </div>
</template>

<script>
import CardMatch from "@/components/CardMatch.vue";

export default {
  components: {
    CardMatch
  }
};
</script>


<style lang="scss" scoped>
#main {
  padding-top: 50px;

  h1 {
    font-weight: 300;
    color: var(--foreground-contrast);
  }
}

.cards-list {
  display: flex;
  flex-wrap: wrap;
  padding: 20px 0;
}
</style>

