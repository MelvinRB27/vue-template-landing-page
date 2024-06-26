<template>
  <v-footer class="footer">
    <div class="div1">
      <div class="logo-container">
        <!-- <v-img height="30" src="@/assets/logo.png" /> -->
        <h1 class="title-footer">Vuetify</h1>
      </div>
      <div>
        <p>
          Copyright © {{ currentYear }}
          <a target="_blank" href="https://dev-melvinrb.vercel.app/"
            >Melvin RB.</a
          >
        </p>
        <p>All rights reserved</p>
      </div>
    </div>

    <div class="div2">
      <div v-for="section in footerSections" :key="section.title">
        <h3>{{ section.title }}</h3>
        <ul>
          <li v-for="item in section.items" :key="item.name">
            <router-link :to="item.link">{{ item.name }}</router-link>
          </li>
        </ul>
      </div>
      <div>
        <h3>Stay up to date</h3>
      </div>
    </div>
  </v-footer>
</template>

<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear(),
      footerSections: [
        {
          title: "Company",
          items: [
            { name: "About us", link: "/about" },
            { name: "Blog", link: "/blog" },
            { name: "Contact us", link: "/contact" },
            { name: "Pricing", link: "/pricing" },
            { name: "Testimonials", link: "/testimonials" },
          ],
        },
        {
          title: "Support",
          items: [
            { name: "Help Center", link: "/help" },
            { name: "FAQ", link: "/faq" },
            { name: "Contact Support", link: "/support" },
            { name: "Community", link: "/community" },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.footer {
  display: flex;
  justify-content: space-between;
  color: #f5f7fa;
  background: #263238;
  height: 328px;
  padding: 20px 100px;
  .div1 {
    display: flex;
    flex-direction: column;
    gap: 20px;
    .logo-container {
      display: flex;
      align-items: center;
    }
    a {
        color: #4CAF4F
    }
  }
  .div2 {
    display: flex;
    gap: 100px;
    > div {
      display: flex;
      flex-direction: column;
      gap: 20px;
      ul {
        list-style-type: none;
        padding: 0;
        li {
          margin: 5px 0;
          a {
            color: #f5f7fa;
            text-decoration: none;
            &:hover {
              text-decoration: underline;
            }
          }
        }
      }
    }
  }
}
.title-footer {
  color: #f5f7fa;
  font-size: 30px;
  padding: 0;
  line-height: 1.2;
}
</style>
