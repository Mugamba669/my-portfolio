<template lang="html">
<div>
    <header :title="title"/>

    <!-- <div id="preloader">
        <div class="loader_line"></div>
    </div> -->
   
    <!-- /PRELOADER -->
    <div class="bg-homeBg dark:bg-homeTwoBg-dark min-h-screen bg-no-repeat bg-center bg-cover bg-fixed md:pb-16 w-full">
        <div class="section-bg">
            <div class="w-full flex justify-between px-4">
                <!-- website Logo -->
                <!-- <a href="/">
                    <img class="h-[26px] lg:h-[32px]" src="@/images/logo/logo.png" alt="logo" />
                </a> -->
                <div class="flex items-center">
                    <!-- dark and light mode toggle -->
                    <button id="theme-toggle" type="button" class="dark-light-btn">
                        <i id="theme-toggle-dark-icon" class="fa-solid text-xl fa-moon hidden"></i>
                        <i id="theme-toggle-light-icon" class="fa-solid fa-sun text-xl hidden"></i>
                    </button>
                    <!-- mobile toggle button -->
                    <button id="menu-toggle" type="button" class="menu-toggle-btn">
                        <i id="menu-toggle-open-icon" class="fa-solid fa-bars text-xl "></i>
                        <i id="menu-toggle-close-icon" class="fa-solid fa-xmark text-xl hidden  "></i>
                    </button>
                </div>
            </div>
        </div>
        <mobile-nav/>
        <!--  -->
               <div class="container grid grid-cols-12 md:gap-10 justify-between lg:mt-[220px]">
                <!-- sidebar -->
                <side-bar/>
                <!-- end of sidebar -->
                  
            <div class="col-span-12 lg:col-span-8">
               <lg-nav/>
         <div>
                 <div class="lg:rounded-2xl bg-white dark:bg-[#111111]">
                    <slot/>
                        <v-footer/>

               </div>
         </div>
            </div>
        </div>
    </div>
</div>
</template>

<script type="text/javascript">
import VFooter from "@/components/footer/footer.vue";
import Header from "@/components/header/header.vue";
import SideBar from "@/components/sidebar/sidebar.vue";
import MobileNav from "@/components/navs/mobile-nav.vue";
import LgNav from "@/components/navs/lg-nav.vue";
import MobileSidebar from "@/components/sidebar/mobile-sidebar.vue";
export default {
  name: "Layout",
  props: ["title"],

  components: {
    Header,
    MobileNav,
    SideBar,
    LgNav,
    MobileSidebar,
    VFooter,
  },
  mounted() {
    document.querySelector(
      "title"
    ).textContent = `${this.title} | Mugamba Bruno`;
  },
};
</script>
<style lang="css">
* {
  user-select: none;
}
@import "@/css/vendor/slick.css";
@import "@/css/custom.css";
@import "@/css/tailwind.css";
</style>