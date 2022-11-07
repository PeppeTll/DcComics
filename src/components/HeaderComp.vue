<template lang="">
    <header>
        <figure>
            <img src="../assets/img/dc-logo.png" alt="">
        </figure>
        <nav>
            <ul>
                <li v-for="(link, i) in navList" :key="i">
                    <a :class="i == index ? 'active': ''" :href="link.href" @click="changeIndex(i)">{{link.nome}}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
  name: "HeaderComp",
  data() {
    return {
      logo: "../assets/img/dc-logo.png",
      navList: [
        {
          nome: "CHARACTERS",
          href: "#",
        },
        {
          nome: "COMICS",
          href: "#",
        },
        {
          nome: "MOVIES",
          href: "#",
        },
        {
          nome: "TV",
          href: "#",
        },
        {
          nome: "GAMES",
          href: "#",
        },
        {
          nome: "COLLECTIBLES",
          href: "#",
        },
        {
          nome: "VIDEOS",
          href: "#",
        },
        {
          nome: "FANS",
          href: "#",
        },
        {
          nome: "NEWS",
          href: "#",
        },
        {
          nome: "SHOP",
          href: "#",
        },
      ],
      index: 0,
      changeIndex: ( i ) => {
        this.index = i
      }
    };
  },
};
</script>

<style lang="scss" scoped>
header {
  padding: 10px;
  margin: 0 auto;
  width: 1024px;
  display: flex;
  justify-content: space-between;

  nav {
    display: flex;
    justify-content: flex-end;
    align-items: center;

    ul {
      list-style: none;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 15px;

      a {
        color: black;
        font-weight: 600;
        text-decoration: none;

        &.active {
          color: rgb(50, 81, 168)
        }
      }
    }
  }
}
</style>