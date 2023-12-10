<template>
  <div>
    <header>
      <Header />
    </header>

    <main>
      <slot />
      <!-- ページコンテンツのスロット -->
    </main>

    <footer>
      <!-- フッターのコンテンツ -->
    </footer>
  </div>
</template>

<script>
export default {
  name: "DefaultLayout",
};
</script>

<style>
/* スタイルの定義 */
</style>
