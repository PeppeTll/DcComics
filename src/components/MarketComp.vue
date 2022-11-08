<template>
  <section>
    <main>
      <ul>
        <li v-for="(object, i) in marketList" :key="i">
          <img :src="require(`../assets/${object.logo}`)" alt="" />
          <a :href="object.href">{{ object.nome }}</a>
        </li>
      </ul>
    </main>
  </section>
</template>

<script>
export default {
  nome: "Market",
  data() {
    return {
      marketList: [
        {
          nome: "DIGITAL COMICS",
          logo: "img/buy-comics-digital-comics.png",
          href: "#",
        },
        {
          nome: "DC MERCHANDISE",
          logo: "img/buy-comics-merchandise.png",
          href: "#",
        },
        {
          nome: "SUBSCRIPTION",
          logo: "img/buy-comics-subscriptions.png",
          href: "#",
        },
        {
          nome: "COMIC SHOP LOCATOR",
          logo: "img/buy-comics-shop-locator.png",
          href: "#",
        },
        {
          nome: "DC POWER VISA",
          logo: "img/buy-dc-power-visa.svg",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixing";

section {
  background-color: rgb(73, 119, 203);

  main {
    @include container;

    ul {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      padding: 0;
      margin: 0;

      li {
        flex-basis: 0;
        flex-grow: 1;
        display: flex;
        gap: 15px;
        align-items: center;

        a {
          font-size: 12px;
          font-weight: 600;
          color: white;
          text-decoration: none;
        }
      }
    }

    img {
      height: 56px;
    }
  }
}
</style>