<template>
  <main class="main">
    <div class="page page_404">
      <div class="container">
        <h1 class="text-center">
          Страница не найдена
          <span>404</span>
        </h1>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'NotFoundPage',
};
</script>

<style scoped>
.page.page_404 {
  padding: 100px 0;
}

.page.page_404 h1 {
  font-family: Nunito, sans-serif;
  font-weight: 700;
  font-size: 52px;
  line-height: 1.2;
  text-align: center;
  color: var(--body-color);
}

.page.page_404 h1 > span {
  display: block;
  font-size: 144px;
}

@media all and (max-width: 767px) {
  .page.page_404 h1 {
    font-size: 36px;
  }

  .page.page_404 h1 > span {
    font-size: 108px;
  }
}
</style>
