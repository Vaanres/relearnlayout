<template>
  <div class="container-fluid">
    <div class="parent d1">
      <div class="cover d1">
        <h1>How to create a facebook cover</h1>
        <h4>With Flexbox & Love</h4>
        <p>By Vaanres</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.parent {
  height: 100vh;
  display: flex;
  place-content: center;
  align-items: center;

  .child {
    height: 100px;
    border: 1px solid black;
  }
}

.cover {
  > * {
    margin: 1rem 0;
  }

  > :first-child:not(h1) {
    margin-top: 0;
  }

  > :last-child:not(h1) {
    margin-bottom: 0;
  }
}
</style>
