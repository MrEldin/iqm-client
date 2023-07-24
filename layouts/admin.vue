<template lang="pug">
  .flex.qbackground-color.min-h-screen
    .w-24.bg-white.flex.flex-col
      NuxtLink.icon-box.flex.items-center.justify-center(to="/dashboard")
        svg-icon.w-20(name="green_logo" width="59" height="42")
      .qmenu.flex.flex-col.items-center.justify-center
        .flex.flex-col
          NuxtLink.icon-box.flex.items-center.justify-center(to="/dashboard")
            svg-icon.w-20.text-gray-700(name="home_icon" width="20" height="20")
          NuxtLink.icon-box.flex.items-center.justify-center(to="/dashboard")
            svg-icon.w-20(name="category_icon" width="20" height="20")
          NuxtLink.icon-box.flex.items-center.justify-center(to="/dashboard")
            svg-icon.w-20(name="users_icon" width="20" height="20")
          NuxtLink.icon-box.flex.items-center.justify-center(to="/dashboard")
            svg-icon.w-20(name="setting_icon" width="20" height="20")
      NuxtLink.icon-box.flex.items-center.justify-center(to="/login")
        svg-icon.w-20(name="logout_icon" width="20" height="20")
    Nuxt
</template>

<style lang="scss">
  .icon-box {
    width: 100%;
    height: 80px;
  }

  .qmenu {
    width: 100%;
    height: calc(100vh - 160px);
  }
</style>
