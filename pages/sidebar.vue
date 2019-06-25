<template>
  <div class="with-sidebar">
    <div class="d-flex flex-wrap">
      <!-- intermediary wrapper -->
      <div class="sidebar">...</div>
      <div class="not-sidebar">...</div>
    </div>
  </div>
</template>

<style lang="scss">
.sidebar {
  flex-basis: 20rem;
  flex-grow: 1;
}

.not-sidebar {
  /* ↓ grow from nothing */
  flex-basis: 0;
  flex-grow: 999;
  min-width: calc(50% - 1rem);
}
</style>
