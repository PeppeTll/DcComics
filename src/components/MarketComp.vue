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
  background-color: rgb(21, 29, 196);

  main {
    @include container;
    padding: 100px 15px;

    ul {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0;

      li {
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 10px;

        a {
          font-size: 12px;
          font-weight: 600;
          color: white;
        }
      }
    }

    img {
      width: 40px;
    }
  }
}
</style>