<template>
  <aside id="sidebar">
    <SearchBox/>

    <nav class="menu">
      <h5>Navigation</h5>
      <ul>
        <li v-for="({ route, title, active, icon }) in menu" :key="route" :class="{active}">
          <img width="24" height="24" :src="icon" :alt="title">
          <p>{{ title }}</p>
        </li>
      </ul>
    </nav>
  </aside>
</template>

<script>
import SearchBox from "@/components/SearchBox.vue";
import home from "@/assets/home.svg";
import live from "@/assets/play-circle-fill.svg";
import favorites from "@/assets/star-fill.svg";

export default {
  components: {
    SearchBox
  },
  data: () => ({
    menu: [
      {
        route: "/",
        title: "Home",
        active: true,
        icon: home
      },
      {
        route: "/live",
        title: "Live",
        active: false,
        icon: live
      },
      {
        route: "/favorites",
        title: "Favorites",
        active: false,
        icon: favorites
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
#sidebar {
  width: 100%;
  height: 100%;
  padding: 25px;

  .menu {
    h5 {
      margin: 30px 0 20px 20px;
      font-size: 0.875rem;
    }

    li {
      display: flex;
      align-items: center;
      height: 50px;
      width: 100%;
      border-radius: 5px;
      margin: 20px 0;
      cursor: pointer;

      > img {
        margin-left: 20px;
      }

      > p {
        margin-left: 10px;
      }

      &:hover {
        background-color: var(--accent);
      }
    }

    .active {
      background-color: var(--accent);
    }
  }
}
</style>


