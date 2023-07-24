<template lang="pug">
  div
    .bg-grey-100.min-h-screen
      .pt-70.pr-70.pl-70.w-full.h-120.flex.iq-bg-green.justify-between
        .h-full.flex.items-center(class="w-6/12")
          .h-full.mr-2.flex.justify-center
            img(src="~/assets/logo.svg")
          h1.text-white.text-4xl iqmanager
        .h-full.flex.items-center.justify-end
          NuxtLink.text-2xl.p-0.text-white.cursor-pointer.transition.delay-150.duration-300.ease-in-out(class="hover:text-gray-500" to="/login") Sign in
      .h-120.px-70.py-8(class="w-4/5")
        .w-full.mb-2
          h1.text-black.text-3xl Raven's Progressive Matrices IQ Test
        div
          p.text-gray-500 Raven's Progressive Matrices or RPM is a nonverbal test typically used to measure general human intelligence and abstract reasoning and is regarded as a non-verbal estimate of fluid intelligence.
      .flex.items-center.justify-center.w-full
        .flex.gap-40.mt-40
          div
            .flex.gap-2.mb-2
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                svg-icon.w-12(name="sample")
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                svg-icon.w-12(name="2")
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                svg-icon.w-12(name="black_up")
            .flex.gap-2.mb-2
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                svg-icon.w-12(name="2")
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                svg-icon.w-12(name="black_up")
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                svg-icon.w-12(name="black_empty_right")
            .flex.gap-2
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                svg-icon.w-12(name="black_up")
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                svg-icon.w-12(name="black_empty_right")
              .test-image.flex.items-center.justify-center.bg-white.rounded-md.shadow
                p.text-5xl.m-0.p-0 ?
          div
            .flex.gap-2.mb-2
              .test-image.flex.items-center.justify-center.bg-white.cursor-pointer.transition.delay-50.duration-200.ease-in-out.rounded-md.shadow(class="hover:bg-blue-50")
                svg-icon.w-12(name="sample")
              .test-image.flex.items-center.justify-center.bg-white.cursor-pointer.transition.delay-50.duration-200.ease-in-out.rounded-md.shadow(class="hover:bg-blue-50")
                svg-icon.w-12(name="2")
              .test-image.flex.items-center.justify-center.bg-white.cursor-pointer.transition.delay-50.duration-200.ease-in-out.rounded-md.shadow(class="hover:bg-blue-50")
                svg-icon.w-12(name="black_up")
            .flex.gap-2.mb-2
              .test-image.flex.items-center.justify-center.bg-white.cursor-pointer.transition.delay-50.duration-200.ease-in-out.rounded-md.shadow(class="hover:bg-blue-50")
                svg-icon.w-12(name="2")
              .test-image.flex.items-center.justify-center.bg-white.cursor-pointer.transition.delay-50.duration-200.ease-in-out.rounded-md.shadow(class="hover:bg-blue-50")
                svg-icon.w-12(name="black_up")
              .test-image.flex.items-center.justify-center.bg-white.cursor-pointer.transition.delay-50.duration-200.ease-in-out.rounded-md.shadow(class="hover:bg-blue-50")
                svg-icon.w-12(name="black_empty_right")
            .flex
              p.text-gray-400 Click on the box that logically best fit.
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
