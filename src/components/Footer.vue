<template>
  <v-footer class="footer">
    <div class="div1">
      <div class="logo-container">
        <v-img width="35" height="24" src="@/assets/IconFooter.svg" />
        <h1 class="title-footer">Nextcent</h1>
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
      <SocialLinks />
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
import SocialLinks from "@/icons/SocialLinks.vue";
export default {
  components: { SocialLinks },
  data() {
    return {
      currentYear: new Date().getFullYear(),
      footerSections: [
        {
          title: "Company",
          items: [
            { name: "About us", link: "#" },
            { name: "Blog", link: "/#" },
            { name: "Contact us", link: "/#" },
            { name: "Pricing", link: "/#" },
            { name: "Testimonials", link: "/#" },
          ],
        },
        {
          title: "Support",
          items: [
            { name: "Help Center", link: "/#" },
            { name: "FAQ", link: "/#" },
            { name: "Contact Support", link: "/#" },
            { name: "Community", link: "/#" },
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
      gap: 1px;
      padding: 0;
    }
    a {
      color: #4caf4f;
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
