<template lang="pug">
  section.container
    div
      logo
      h1.title
        vue-static-site
      h2.subtitle
        | Nuxt.js project
      .links
        a.button--green(
          href="https://nuxtjs.org/"
          target="_blank")
          | Documentation
        a.button--grey(
          href="https://github.com/nuxt/nuxt.js"
          target="_blank")
          | GitHub
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  asyncData (context) {
    // The most important key, it can be asynchronous and receives the context as argument,
    // please read the async data documentation https://nuxtjs.org/guide/async-data
    // called every time before loading the component
    return { name: 'World' }
  },
  fetch () {
    // Used to fill the store before rendering the page, 
    // it's like the data method except it doesn't set the component data.
    // See the API Pages fetch documentation. https://nuxtjs.org/api/pages-fetch
  },
  head () {
    // Set specific Meta Tags for the current page, see API Pages head 
    // documentation. https://nuxtjs.org/api/pages-head
  },
  layout () {
    // Specify a layout defined in the layouts directory, 
    // see API Pages layout documentation https://nuxtjs.org/api/pages-layout
  },
  transition () {
    // Set a specific transition for the page, see API Pages transition.
    // https://nuxtjs.org/api/pages-transition
  },
  scrollToTop () {
    // Boolean, by default: false. 
    // Specify if you want the page to scroll to the top 
    // before rendering the page, it's used for nested routes.
  },
  validate () {
    // Validator function for dynamic routes. 
    // https://nuxtjs.org/guide/routing#dynamic-routes
  },
  middleware () {
    // Set a middleware for this page, 
    // the middleware will be called before rendering the page, 
    // see routes middleware. https://nuxtjs.org/guide/routing#middleware
  },
  // HOOKS
  beforeCreate () {
    // Called synchronously immediately after the instance has been initialized,
    // before data observation and event/watcher setup.
  },
  created () {
    // Called synchronously after the instance is created. 
    // At this stage, the instance has finished processing the options 
    // which means the following have been set up: 
    // data observation, computed properties, methods, watch/event callbacks. 
    // However, the mounting phase has not been started, 
    // and the $el property will not be available yet.
  },
  beforeMount () {
    // Called right before the mounting begins: 
    // the render function is about to be called for the first time.
  },
  mounted () {
    // Called after the instance has been mounted, 
    // where el is replaced by the newly created vm.$el. 
    // If the root instance is mounted to an in-document element, 
    // vm.$el will also be in-document when mounted is called.
  },
  beforeUpdate () {
    // Called when the data changes, before the virtual DOM is re-rendered
    // and patched.
  },
  updated () {
    // Called after a data change causes the virtual DOM 
    // to be re-rendered and patched.
    // The component’s DOM will have been updated when this hook is called, 
    // so you can perform DOM-dependent operations here. 
    // However, in most cases you should avoid changing state inside the hook.
    // To react to state changes, it’s usually better to use a computed 
    // property or watcher instead.
  },
  activated () {
    // Called when a kept-alive component is activated.
  },
  deactivated () {
    // Called when a kept-alive component is deactivated.
  },
  beforeDestroy () {
    // Called right before a Vue instance is destroyed. 
    // At this stage the instance is still fully functional.
  },
  destroyed () {
    // Called after a Vue instance has been destroyed. 
    // When this hook is called, all directives of the 
    // Vue instance have been unbound, all event listeners 
    // have been removed, and all child Vue instances 
    // have also been destroyed.
  }
}
</script>

<style lang="scss">
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  .title {
    font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }
  .subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
  }
  .links {
    padding-top: 15px;
  }
}
</style>
