<template>
  <div class="social-icons">
    <a href="https://www.linkedin.com/in/prashant-ranjan-2617926a">
      <font-awesome-icon :icon="['fab', 'linkedin']" size="2x" />
    </a>
    <a href="https://www.facebook.com/prashant.ranjan.1272">
      <font-awesome-icon :icon="['fab', 'facebook']" size="2x" />
    </a>
    <a href="https://twitter.com/prashant_344">
      <font-awesome-icon :icon="['fab', 'twitter']" size="2x" />
    </a>
    <a href="https://www.instagram.com/prashant_ranjan344/">
      <font-awesome-icon :icon="['fab', 'instagram']" size="2x" />
    </a>
  </div>
</template>

<script>
export default {
  name: "SocialLinks"
}
</script>>
<style scoped>
.social-icons {
  display: flex;
  align-items: center;
  justify-content: center;
}
a {
  color: #fff;
  padding: 10px;
  transition: all 0.5s ease;
}
a:hover {
  color: #1cb698;
  transition: all 0.5s ease;
}
</style>>