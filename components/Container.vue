<template>
  <div class="container" :class="{ 'container--full': full }">
    <div class="container__inner">
      <slot></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  full?: boolean
}>()
</script>

<style lang="sass">
.container
  --content-max-width: 75rem
  --content-padding: 2rem
  --container-margin: 0 auto
  width: 100%
  margin: var(--container-margin)

  &__inner
    margin: 0 auto
    padding: 0 var(--content-padding)
    width: 100%
    max-width: var(--content-max-width)

    @include responsive(mobile)
      padding: 0 1rem

  &--full
    .container__inner
      max-width: none
      padding: 0

    @include responsive(mobile)
      .container__inner
        padding: 0

  // Breakout functionality
  &:not(&--full)
    .breakout
      width: 100vw
      margin-left: 50%
      transform: translateX(-50%)
      position: relative

      @include responsive(mobile)
        width: 100%
        margin-left: 0
        transform: none
</style>