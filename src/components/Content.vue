<script setup>
import Logo from "./Logo.vue";
import VerticalLine from "./VerticalLine.vue";
import Social from "./Socials.vue";
</script>

<template>
  <div class="container">
    <Logo />
    <VerticalLine />
    <Social :socials="socials" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      socials: [
        {
          text: "LinkedIn",
          icon: { family: "fab", name: "linkedin" },
          link: "https://de.linkedin.com/in/ilyas-keskin-6697a518a",
        },
        {
          text: "Xing",
          icon: { family: "fab", name: "square-xing" },
          link: "https://www.xing.com/profile/Ilyas_Keskin3",
        },
        {
          text: "Credly",
          icon: { family: "fas", name: "certificate" },
          link: "https://www.credly.com/users/ilyas-keskin.a35bbfee/badges",
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row-reverse;
  align-items: center;
  justify-content: space-between;
  min-width: 600px;
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
}

@media (max-width: 430px) {
  .container {
    flex-direction: column;
    justify-content: center;
    min-width: 0;
  }
}
</style>
