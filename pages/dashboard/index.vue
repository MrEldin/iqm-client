<template lang="pug">
  .w-full.min-h-screen.flex
    .main-page
    .right-sidebar.bg-white.h-full.px-10
      .flex.flex-col.h-20.w-full.justify-center
        .flex.items-center.justify-left
          h1.text-xl.text-gray-500 Eldin Mujovic
        .flex.items-center.justify-left
          h1.text-xs.text-gray-400 eldinpc@live.com
      .flex.flex-col.w-full.items-center.mb-28
        .flex.w-full.items-center.justify-between.mb-3
          h1.text-gray-600.text-lg Top Users
          a.text-sm(href="#") Show all
        .flex.flex-col.w-full
          .flex.w-full.items-center.justify-between.h-8.border-b-2.border-gray-50(v-for="(user, index) in users" :key="index")
            .flex
              p.text-gray-500.text-xs.mb-0.w-6 {{index+1}}
              p.text-gray-500.text-xs.mb-0 {{user.name}}
            p.text-gray-500.text-xs.mb-0 {{user.score}}
      .flex.flex-col.h-auto.w-full.items-center.qbg.rounded-3xl.p-10
        .relative.flex.flex-col.w-full.items-center.iltop
          svg-icon.mb-6(name="world_illustration")
          h1.text-lg.text-white.mb-4 How are you today, maybe you should create a new test?
          p.text-base.text-white.text-opacity-70 Did you know that every test that you create, you are helping world to be smarter.
          .flex.w-full.justify-center
            nuxt-link(to="/test" class="text-white py-2 px-6 rounded-full inline-flex items-center hover:bg-grey bg-white")
              svg-icon(class="w-5 h-5 mr-1" name="idea_icon")
              span(class="whitespace-nowrap text-black") Create new test
</template>

<script>
  export default {
    layout: 'admin',
    data: function () {
      return {
        users: [
          {
            name: 'John Doe',
            score: 142
          },
          {
            name: 'Eldin Mujovic',
            score: 132
          },
          {
            name: 'Demir Dautovic',
            score: 124
          },
          {
            name: 'Pedro Gorgovski',
            score: 123
          },
          {
            name: 'Mauricius Bartmen',
            score: 123
          },
          {
            name: 'Sergio Derdani',
            score: 118
          },
          {
            name: 'Marko Polo',
            score: 116
          },
          {
            name: 'Jack Gordon Harris',
            score: 110
          },
          {
            name: 'Ukica Pikaso',
            score: 111
          },
          {
            name: 'Dejana Martinovic',
            score: 100
          }
        ]
      }
    },
  }
</script>

<style lang="scss">
  .test-image {
    height: 114px;
    width: 115px;
  }
  .right-sidebar {
    width: 370px;
  }
  .main-page {
    height: 100%;
    width: calc(100% - 360px);
  }

  .qbg {
    background-image: linear-gradient(220deg, #00796B 30%, #01579B);
  }

  .iltop {
    margin-top: -140px;
  }
</style>
