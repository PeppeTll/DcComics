<template>
  <div>
    <section id="topFooter">
      <footer>
        <div>
          <ul>
            <h3>DC Comics</h3>
            <li v-for="(object, i) in dcComics" :key="i">
              <a :href="object.href">{{ object.nome }}</a>
            </li>
          </ul>
          <ul>
            <h3>DC</h3>
            <li v-for="(object, i) in dc" :key="i">
              <a :href="object.href">{{ object.nome }}</a>
            </li>
          </ul>
          <ul>
            <h3>Sites</h3>
            <li v-for="(object, i) in sites" :key="i">
              <a :href="object.href">{{ object.nome }}</a>
            </li>
          </ul>
          <ul>
            <h3>Shop</h3>
            <li v-for="(object, i) in shop" :key="i">
              <a :href="object.href">{{ object.nome }}</a>
            </li>
          </ul>
        </div>
        <img :src="require(`../assets/${logo}`)" alt="" class="logo" />
      </footer>
    </section>
    <section id="bottomFooter">
      <div class="container">
        <div>
        <button type="submit">sing-up now!</button>
      </div>
      <div class="iconWrap">
        <h3><a href="#">{{follow}}</a></h3>
        <ul>
          <li v-for="(el, i) in icons" :key="i">
          <img :src="require(`../assets/${el.icon}`)" alt="">
          </li>
        </ul>
      </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "FooterComp",
  data() {
    return {
      dcComics: [
        {
          nome: "Characters",
          href: "#",
        },
        {
          nome: "Comics",
          href: "#",
        },
        {
          nome: "Movies",
          href: "#",
        },
        {
          nome: "TV",
          href: "#",
        },
        {
          nome: "Games",
          href: "#",
        },
        {
          nome: "Videos",
          href: "#",
        },
        {
          nome: "News",
          href: "#",
        },
      ],
      shop: [
        {
          nome: "Shop DC",
          href: "#",
        },
        {
          nome: "Shop DC Collectibles",
          href: "#",
        },
      ],
      dc: [
        {
          nome: "Terms Of Use",
          href: "#",
        },
        {
          nome: "Privaci policy (New)",
          href: "#",
        },
        {
          nome: "Ad Choices",
          href: "#",
        },
        {
          nome: "Advertsing",
          href: "#",
        },
        {
          nome: "Jobs",
          href: "#",
        },
        {
          nome: "Subscriptions",
          href: "#",
        },
        {
          nome: "talent Workshops",
          href: "#",
        },
        {
          nome: "CPSC Certificates",
          href: "#",
        },
        {
          nome: "Ratings",
          href: "#",
        },
        {
          nome: "Shop Help",
          href: "#",
        },
        {
          nome: "Contact Us",
          href: "#",
        },
      ],
      sites: [
        {
          nome: "DC",
          href: "#",
        },
        {
          nome: "Mad Magazine",
          href: "#",
        },
        {
          nome: "DC Kids",
          href: "#",
        },
        {
          nome: "DC Universe",
          href: "#",
        },
        {
          nome: "DC Power Visa",
          href: "#",
        },
      ],
      logo: "img/dc-logo-bg.png",
      follow: 'follow us',
      icons: [
        {
          icon: 'img/footer-facebook.png'
        },
        {
          icon: 'img/footer-twitter.png'
        },
        {
          icon: 'img/footer-youtube.png'
        },
        {
          icon: 'img/footer-pinterest.png'
        },
        {
          icon: 'img/footer-periscope.png'
        },
      ]
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixing";
#topFooter {
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;

  footer {
    @include container;
    position: relative;
    overflow: hidden;

    div {
      display: flex;
      flex-wrap: wrap;
      justify-content: flex-start;
      max-width: calc(100% / 3);

      h3 {
        color: white;
      }

      a {
        color: white;
        font-size: 12px;
        text-decoration: none;
      }
    }

    .logo {
      position: absolute;
      right: 0;
      top: -3%;
    }
  }
}

#bottomFooter {
  background-color: rgb(28, 28, 33);

  .container {
    @include container;
    display: flex;
    justify-content: space-between;

    button {
      background-color: rgb(28, 28, 33);
      color: white;
      text-transform: uppercase;
      padding: 10px;
      border-color: rgb(73, 119, 203);
    }

    .iconWrap {
      display: flex;
      gap: 20px;
      text-transform: uppercase;

      a {
        text-decoration: none;
        color: rgb(73, 119, 203);
      }

      ul {
        display: contents;
      }
    }
  }
}
</style>