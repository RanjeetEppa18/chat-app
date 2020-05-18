<template>
  <!-- eslint-disable vue/no-v-html -->
  <component :is="type" v-html="svg" />
  <!--eslint-enable-->
</template>

<script>
const req = require.context(
  '!!raw-loader!../assets/svg_icons/',
  true,
  /^\.\/.*\.svg$/
)

/**
 * Icons are used to visually communicate core parts of the product and
 * available actions. They can act as wayfinding tools to help users more
 * easily understand where they are in the product.
 */
export default {
  name: 'Icon',
  props: {
    /**
     * The name of the icon to display.
     */
    name: {
      type: String,
      required: true,
      default: 'settings'
    },
    /**
     * The fill color of the SVG icon.
     */
    fill: {
      type: String,
      default: 'currentColor'
    },
    color: {
      type: String
    },
    fontSize: {
      type: String,
      default: '2rem'
    },
    width: {
      type: String,
      default: 'auto'
    },
    /**
     * Descriptive text to be read to screenreaders.
     */
    ariaLabel: {
      type: String,
      default: 'icon'
    },
    /**
     * The html element name used for the icon.
     */
    type: {
      type: String,
      default: 'span'
    },
    /**
     * The size of the icon. Defaults to medium.
     * `small, medium, large`
     */
    size: {
      type: String,
      default: 'small',
      validator: value => {
        return value.match(/(small|medium|large|wide)/)
      }
    },
    /**
     * Manually trigger various states of the muted-link.
     * `hover, active, focus`
     */
    state: {
      type: String,
      default: null,
      validator: value => {
        return value.match(/(hover|active|focus)/)
      }
    }
  },
  computed: {
    svg() {
      return req('./' + this.name + '.svg').default.replace(
        /^<svg /,
        `<svg style="fill: ${this.fill};color:${this.color};font-size:${this.fontSize}" `
      )
    }
  }
}
</script>

<style lang="css" scoped="">
.icon {
  vertical-align: middle;
  cursor: pointer;
}
.wide {
  width: 24px;
  height: 14px;
}
.large {
  height: 64px;
  width: 64px;
}

.medium {
  width: 24px;
  height: 24px;
}
.small {
  width: 14px;
  height: 14px;
}
</style>
