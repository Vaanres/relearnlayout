<template>
  <main class="wrapper">
    <section class="section parallax bg1">
      <h1>Background 1</h1>
    </section>
    <section class="section static">
      <h1>Here is the content. No effect</h1>
    </section>
    <section class="section parallax bg2">
      <h1>Background 2</h1>
    </section>
  </main>
</template>

<style lang="scss">
.wrapper {
  /* The height needs to be set to a fixed value for the effect to work.
   * 100vh is the full height of the viewport. */
  height: 100vh;
  /* The scaling of the images would add a horizontal scrollbar, so disable x overflow. */
  overflow-x: hidden;
  /* Enable scrolling on the page. */
  overflow-y: auto;
  /* Set the perspective to 2px. This is essentailly the simulated distance from the viewport to transformed objects.*/
  perspective: 2.5px;
}

.section {
  /* Needed for children to be absolutely positioned relative to the parent. */
  position: relative;
  /* The height of the container. Must be set, but it doesn't really matter what the value is. */
  height: 100vh;
}

.parallax::after {
  /* Display and position the pseudo-element */
  content: ' ';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;

  /* Move the pseudo-element back away from the camera,
   * then scale it back up to fill the viewport.
   * Because the pseudo-element is further away, it appears to move more slowly, like in real life. */
  transform: translateZ(-1.5px) scale(2);
  /* Force the background image to fill the whole element. */
  background-size: 100%;
  /* Keep the image from overlapping sibling elements. */
  z-index: -1;
}

.static {
  background: gray;
}

.bg1::after {
  background-image: url('https://placekitten.com/g/900/700');
}

.bg2::after {
  background-image: url('https://placekitten.com/g/800/600');
}
</style>
