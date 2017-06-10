<template lang="pug">
  #navigation
    h5 project-name
    nav
      ul
        li
          .component
            span.status
            span.label
              a(href="#") @include
            span.action
              img.btn(src="static/icons/menu-dots-white.svg")
              .popup
        li
          .component
            span.status
            span.label
              a(href="#") body
            span.action
              img.btn(src="static/icons/menu-dots-white.svg")
              .popup
          ul
            li
              .component
                span.status
                span.label
                  a(href="#") header
                span.action
                  img.btn(src="static/icons/menu-dots-white.svg")
                  .popup
            li
              .component
                span.status
                span.label
                  a(href="#") footer
                span.action
                  img.btn(src="static/icons/menu-dots-white.svg")
                  .popup
</template>

<script>
export default {
  props: {
    // key: value,
  },
  data () {
    return {
      // key: ObjectType
    }
  },
  ready () {
    // key: value,
  },
  methods: {
    //
  }
}
</script>

<style lang="sass" scoped>
  @import '../assets/style/config'
  @import '../assets/style/mixins'

  // component logic
  #navigation nav
    li
      // display: flex
      // align-items: stretch
    span.status:before
      content: "\00B7"
      margin-right: 0.25rem
      font-size: 2rem
      font-weight: 700
      display: inline-block
      color: #666
    span
      line-height: 1.5rem
      height: 1.5rem
      img
        height: 70%
        padding: 15% 0

  // layout
  #navigation nav
    display: flex
    flex-direction: column
    align-items: stretch
    li .component
      flex: 1
      display: flex
      align-items: center
      span.label
        flex: 1

  // position
  #navigation
    position: fixed
    top: 0
    left: 0
    bottom: 0

  // width-height
  #navigation
    min-width: 12rem

  // spacing
  #navigation
    padding: 0.5rem
    nav ul
      @include reset-space
      list-style: none
      ul
        margin-left: 1rem
    nav li .component
      padding: 0.25rem 0 0.25rem 0.5rem

  // typography
  #navigation
    text-align: left
    font-size: 80%

  // colors
  #navigation
    background: #333
    color: #FFF
    li
      color: #FFF
      a
        color: #FFF
      .component
        @include activate-background
      span.label
        @include activate-opacity(0.7)
      span.action
        opacity: 0.2
        &:hover
          opacity: 1


</style>
