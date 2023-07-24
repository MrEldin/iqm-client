<template lang="pug">
  .flex.iq-bg-green.min-h-screen
    .min-h-screen.p-16(class="w-1/3")
      .w-full.bg-white.h-full.rounded-xl
        div(class="h-1/3")
          .w-full.h-full.flex.items-center.justify-center
            h-full.mr-2.flex.justify-center
              svg-icon.w-20(name="logo_black")
            h1.text-black.text-4xl iqmanager
        div(class="h-2/3")
          div.px-20.pb-5
            label Email:
            input(type="text" placeholder="Enter your email" class="px-3 py-3 placeholder-gray-400 text-gray-700 relative bg-gray-100 rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full")
          div.px-20.pb-5
            label Password:
            input(type="password" placeholder="Enter your password" class="px-3 py-3 placeholder-gray-400 text-gray-700 relative bg-gray-100 bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full")
          div.px-20.pb-5
            nuxt-link(to="/test" class="iq-button w-full text-white py-3 px-10 rounded inline-flex items-center border-2 hover:bg-grey flex justify-center")
              svg-icon(class="w-6 h-6 mr-3" name="idea_icon")
              span(class="whitespace-nowrap") Login
    .flex.justify-center(class="w-2/3")
      svg-icon(class="w-1/2" name="hero_illustration")
</template>

<script>
  export default {}
</script>

<style lang="scss">
  .test-image {
    height: 114px;
    width: 115px;
  }
</style>
