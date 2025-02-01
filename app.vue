<template>
  <div>
    <Container>
      <div style="background: red; padding: 2rem;">
        <h1>Regular Container</h1>
      </div>
    </Container>

    <Container full>
      <div style="background: blue; padding: 2rem; color: white;">
        <h1>Full Width Container</h1>
      </div>
    </Container>

    <Container>
      <div style="background: green; padding: 2rem; color: white;">
        <h1>Regular Content</h1>
      </div>
      <div class="breakout" style="background: purple; padding: 2rem; color: white;">
        <div style="max-width: 75rem; margin: 0 auto;">
          <h1>Breakout Content</h1>
        </div>
      </div>
    </Container>
  </div>
</template>

<style lang="sass">
@import "~/assets/styles/main"
</style>