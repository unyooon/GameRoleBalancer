<template>
  <div class="header">
    <div class="header__logo">
      <NuxtLink to="/">SkillSync Matchmaker</NuxtLink>
    </div>
    <div class="header__nav">
      <Button
        text="Home"
        :active="route.fullPath === '/'"
        @onClick="() => router.push('/')"
      />
      <Button
        text="OverWatch"
        :active="route.fullPath === '/ow'"
        @onClick="() => router.push('/ow')"
      />
    </div>
  </div>
</template>

<script lang="ts" setup>
const route = useRoute();
const router = useRouter();
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 72px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: $background-color--header;
  padding: 0 24px;

  &__logo {
    a {
      text-decoration: none;
      color: $text-color--body;
      font-weight: 600;
      font-size: 18px;
    }
  }

  &__nav {
    display: flex;

    div {
      margin: 0 8px;
    }
  }
}

@media screen and (max-width: 768px) {
  .header {
    height: 120px;
    padding: 16px;
    flex-direction: column;

    &__logo {
      a {
        // font-size: 16px;
      }
    }
  }
}
</style>
