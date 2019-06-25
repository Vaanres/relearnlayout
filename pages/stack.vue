<template>
  <div class="container">
    <h1>Stack</h1>

    <div class="stack">
      <div><!-- child --></div>
      <div><!-- child --></div>
      <div class="stack">
        <div>1</div>
        <div>1</div>
        <div>1</div>
      </div>
      <div><!-- etc --></div>
    </div>
  </div>
</template>

<style lang="scss">
[class^='stack'] > * {
  margin: 0;
}
.stack {
  --space: 1.5rem;

  & * {
    background: transparentize(#000000, 0.9);
    min-height: 50px;
  }

  & * + * {
    margin-top: var(--space);
  }
}
</style>
