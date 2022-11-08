<template lang="">
    <header>
        <figure>
            <img src="../assets/img/dc-logo.png" alt="">
        </figure>
        <nav>
            <ul>
                <li v-for="(link, i) in navList" :key="i" :class="i == index ? 'active': ''" @click="changeIndex(i)">
                    <a  :href="link.href" >{{link.nome}}</a>
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
      changeIndex: (i) => {
        this.index = i;
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import '../assets/scss/mixing';

header {
  @include container;
  padding: 0;
  display: flex;
  justify-content: space-between;
  min-height: 118px;

  figure {
    align-self: center;
    margin: 0;
  }

  nav {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;

    ul {
      list-style: none;
      display: contents;
      margin: 0;

      li {
        a {
          color: currentColor;
          font-weight: 600;
          text-decoration: none;
          height: 100%;
          display: flex;
          align-items: center;
          position: relative;
        }

        &.active, &:hover {
          color: rgb(73, 119, 203);

          a::after {
            content: '';
            display: block;
            height: 4px;
            position: absolute;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgb(73, 119, 203);
            }
          }
        }
      }
    }
  }
</style>