<template>
  <div class="grid">
    <div class="content">content</div>
    <div class="content2">content 2</div>
  </div>
</template>

<style lang="scss" scoped>
body {
  margin: 0;
  padding: 2em;
  font: 125% 'Open sans', sans-serif;
}

.grid {
  display: grid;
  border: 2px solid rgb(124, 222, 220);
  gap: 20px;
  grid-template-rows: 100px auto 100px;
  grid-template-columns:
    minmax(0, 1fr)
    minmax(0, 1fr) [content-start]
    minmax(0, 2fr)
    minmax(0, 2fr) [content-end]
    minmax(0, 1fr)
    minmax(0, 1fr);
}

.grid > * {
  background-color: rgb(114, 132, 168);
  color: #fff;
  padding: 1em;
  margin: 0;
}

.content {
  grid-row: 2;
  grid-column: content-start / content-end;
}

.content2 {
  grid-row: 3;
  grid-column: content-start / content-end;
}
</style>
