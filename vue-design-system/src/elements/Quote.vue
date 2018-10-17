<template>
  <component :is="type" class="quote">
    <slot />
  </component>
</template>

<script>
/**
 * Used to build the outer wrapper of a page, including the page title and
 * associated actions. Wrapper doesn’t provide customizable options.
 */
export default {
  name: "Quote",
  status: "review",
  release: "1.0.0",
  props: {
    /**
     * The html element name used for the wrapper.
     */
    type: {
      type: String,
      default: "blockquote",
    },
  },
}
</script>

<style lang="scss" scoped>
.quote {
  @include reset;
  @include inset-space($space-l);
  font-family: $font-text;
  font-weight: $weight-light;
  font-size: $size-l;
  line-height: $line-height-m;
  width: 100%;
  @media #{$media-query-l} {
    @include inset-space($space-xl);
  }
}
</style>


<docs>
  ```jsx
  <Quote>In addition there comes out from the sea from time to time a hand of steel which plucks the German sentries from their posts with growing efficiency, amid the joy of the whole countryside.</Quote>
  ```
</docs>
