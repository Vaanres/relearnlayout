<template>
  <div class="container">
    <article>
      <h1>Here's a Header</h1>
      <p>I'm a paragraph with all kinds of information.</p>
      <p>Let's add another paragraph for fun.</p>
      <p>yadda yadda yadda</p>
      <p>blah blah blah</p>
      <p>yadda yadda yadda</p>
      <h3>Here's a Subheader</h3>
      <p>blah blah blah</p>
      <p>And maybe just one more.</p>
    </article>
  </div>
</template>

<style lang="scss" scoped>
article {
  p:nth-of-type(2n) {
    color: indianred;
  }
}
</style>
