<template>
  <div>
    <div class='echo relative h-screen'>
      <div class="header__bg absolute top-0 bottom-0 right-0 left-0 w-full h-full transform -skew-y-6 origin-top-left"></div>
      <div class="relative pr-70 pl-70 w-full h-120 flex pt-10">
        <div class="w-6/12 h-full flex items-center">
          <div class="h-full mr-2 flex justify-center">
            <img src="~/assets/logo.svg"/>
          </div>

          <h1 class="text-white text-4xl">iqmanager</h1>
        </div>
        <div class="w-6/12 h-full flex items-center justify-end">
          <NuxtLink
            class="text-2xl p-0 text-white hover:text-gray-500 cursor-pointer transition delay-150 duration-300 ease-in-out"
            to="/login">Sign in
          </NuxtLink>
        </div>
      </div>
      <section class="relative w-full h-550 pr-70 pl-70 flex items-center">

        <div class="w-7/12 h-72">
          <div class="mb-70">
            <h1 class="text-3xl text-white pb-4">Check your IQ completely anonymously.</h1>
            <p class="text-xl text-greenblue">You will be able to get your IQ level completely anonymously. After test
              is finished you will decide if
              test is going to be public or not!</p>
          </div>
          <nuxt-link to="/test"
                     class="iq-button text-white py-3 px-10 rounded-full inline-flex items-center border-2 hover:bg-grey">
            <svg-icon class="w-6 h-6 mr-3" name="idea_icon"></svg-icon>
            <span class="whitespace-nowrap">Start your brain</span>
          </nuxt-link>
        </div>
        <div class="w-5/12 h-full flex justify-end items-center invisible md:visible">
          <svg-icon class="w-full h-full" name="hero_illustration"></svg-icon>
        </div>
      </section>
      <section class="qbackground-color w-full h-400 pr-70 pl-70 flex justify-center">
        <div class="flex justify-center items-center flex-wrap gap-70">
          <pricebox
            :price="'Free'"
            :description="'If you want to check you IQ and to be in the list for competitive users. And want to have a proof that you are a smart man, and to find where are you in the smart world.'"
          />
          <pricebox
            :currency="'$'"
            :price_type="'PRO'"
            :primary="true"
            :price="'1'"
            :description="'You know behind this project stays a lot of psychologists and a lot of programmers, if you want to buy a one of them a coffee, this is a way to do that.'"
          />
          <pricebox
            :currency="'$'"
            :price_type="'ULTIMATE'"
            :price="'5'"
            :description="'You know behind this project stays a lot of psychologists and a lot of programmers, if you want to buy a coffee to all team, this is a way to do that.'"
          />
        </div>
      </section>
    </div>

    <section class="w-full mt-52 pr-70 pl-70 qbackground-color">
      <user-box v-for="user in [1,2,3,4,5,6,7,8,9]" :key="user"/>
    </section>


    <footer class="relative h-80 mt-20 overflow-hidden qbackground-color">
      <div
        class="footer__bg absolute bottom-0 right-0 left-0 top-0 w-full h-full transform skew-y-3 origin-top-left"></div>
      <div class="relative flex">
        <svg-icon class="relative w-550 h-400" name="big_hidden_logo"></svg-icon>
        <div class="absolute bottom-0 flex flex-col justify-end items-center w-full py-16">
          <p class="text-white">Copyright 2021</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
  import Pricebox from "../components/pricebox";
  import UserBox from "../components/user-box";

  export default {
    components: {UserBox, Pricebox}
  }
</script>

<style lang="scss">
  .echo {

    .header__bg {
      background-image: linear-gradient(220deg, #00796B 56%, #01579B);
    }
  }

  .footer__bg {
    background-image: linear-gradient(220deg, #00796B 56%, #01579B);
  }
</style>

