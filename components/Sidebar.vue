<template>
  <aside id="sidebar">
    <SearchBox/>

    <nav class="menu">
      <h5>Navigation</h5>
      <ul>
        <li
          v-for="({ route, title, active, icon }) in menuNavigation"
          :key="route"
          :class="{active}"
        >
          <img width="24" height="24" :src="icon" :alt="title">
          <p>{{ title }}</p>
        </li>
      </ul>
    </nav>

    <nav class="menu">
      <h5>Sports</h5>
      <ul>
        <li v-for="({ route, title, active, icon }) in menuSports" :key="route" :class="{active}">
          <img width="20" height="20" :src="icon" :alt="title">
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
import soccer from "@/assets/football.svg";

export default {
  components: {
    SearchBox
  },
  data: () => ({
    menuNavigation: [
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
    ],
    menuSports: [
      {
        route: "/soccer",
        title: "Soccer",
        active: false,
        icon: soccer
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
#sidebar {
  width: 100%;
  height: 100%;
  padding: 25px 10px;

  .menu {
    h5 {
      margin: 30px 0 20px 20px;
      font-size: 0.875rem;
      color: var(--accent-contrast);
    }

    li {
      display: flex;
      align-items: center;
      height: 50px;
      width: 100%;
      border-radius: 5px;
      margin: 20px 0;
      cursor: pointer;
      overflow: hidden;
      animation: none;

      > img {
        margin-left: 20px;
      }

      > p {
        margin-left: 10px;
      }

      &:hover {
        background-color: var(--accent);
        animation: pulse 0.5s ease-in;
      }
    }

    .active {
      background-color: var(--accent);
    }
  }
}
</style>


