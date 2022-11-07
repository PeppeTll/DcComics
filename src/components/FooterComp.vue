<template>
  <section>
    <footer>
      <div>
        <ul>
          <h2>DC Comics</h2>
          <li v-for="(object, i) in dcComics" :key="i">
            <a :href="object.href">{{object.nome}}</a>
          </li>
        </ul>
        <ul>
          <h2>DC</h2>
          <li v-for="(object, i) in dc" :key="i">
            <a :href="object.href">{{object.nome}}</a>
          </li>
        </ul>
        <ul>
          <h2>Sites</h2>
          <li v-for="(object, i) in sites" :key="i">
            <a :href="object.href">{{object.nome}}</a>
          </li>
        </ul>
        <ul>
          <h2>
            Shop
          </h2>
          <li v-for="(object, i) in shop" :key="i">
            <a :href="object.href">{{object.nome}}</a>
          </li>
        </ul>
      </div>
      <img :src="require(`../assets/${logo}`)" alt="" class="logo">
    </footer>
  </section>
</template>

<script>
export default {
  name: "FooterComp",
  data() {
    return {
      dcComics: [
        {
          nome: 'Characters',
          href: '#'
        },
        {
          nome: 'Comics',
          href: '#'
        },
        {
          nome: 'Movies',
          href: '#'
        },
        {
          nome: 'TV',
          href: '#'
        },
        {
          nome: 'Games',
          href: '#'
        },
        {
          nome: 'Videos',
          href: '#'
        },
        {
          nome: 'News',
          href: '#'
        },
      ],
      shop: [
        {
          nome: 'Shop DC',
          href: '#'
        },
        {
          nome: 'Shop DC Collectibles',
          href: '#'
        },
      ],
      dc: [
        {
          nome: 'Terms Of Use',
          href: '#'
        },
        {
          nome: 'Privaci policy (New)',
          href: '#'
        },
        {
          nome: 'Ad Choices',
          href: '#'
        },
        {
          nome: 'Advertsing',
          href: '#'
        },
        {
          nome: 'Jobs',
          href: '#'
        },
        {
          nome: 'Subscriptions',
          href: '#'
        },
        {
          nome: 'talent Workshops',
          href: '#'
        },
        {
          nome: 'CPSC Certificates',
          href: '#'
        },
        {
          nome: 'Ratings',
          href: '#'
        },
        {
          nome: 'Shop Help',
          href: '#'
        },
        {
          nome: 'Contact Us',
          href: '#'
        },
      ],
      sites: [
        {
          nome: 'DC',
          href: '#'
        },
        {
          nome: 'Mad Magazine',
          href: '#'
        },
        {
          nome: 'DC Kids',
          href: '#'
        },
        {
          nome: 'DC Universe',
          href: '#'
        },
        {
          nome: 'DC Power Visa',
          href: '#'
        },
      ],
      logo: 'img/dc-logo-bg.png'
    }
  },
};
</script>

<style lang="scss" scoped>
@import '../assets/scss/mixing';
  section {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    background-repeat: no-repeat;

    footer{
      @include container;
      padding: 70px 0;
      position: relative;
      overflow: hidden;

      div {
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
        max-width: 50%;
        font-size: 10px;

        h2 {
          color: white;
        }

        a {
          color: white;
        }
      }

      .logo {
          position: absolute;
          right: 0;
          top: -12%;
        }
    }
  }
</style>