<template lang="html">
      <!-- sidber personal info -->
            <div class="col-span-12 lg:col-span-4 hidden lg:block h-screen sticky top-44">
                <div
                    class="w-full mb-6 lg:mb-0 mx-auto relative bg-white text-center dark:bg-[#111111] px-6 rounded-[20px] mt-[180px] md:mt-[220px] lg:mt-0">
                    <!-- profile image -->
                    <img src="@/assets/dp.jpg"
                        class="w-[240px] absolute left-[50%] transform -translate-x-[50%] h-[240px] drop-shadow-xl mx-auto rounded-[20px] -mt-[140px]"
                        alt="about" />
                    <div class="pt-[100px] pb-8">
                        <h2 class="mt-6 mb-1 text-[26px] font-semibold dark:text-white"> Mugamba Bruno M.H </h2>
                        <h3
                            class="mb-4 text-[#7B7B7B] inline-block dark:bg-[#1D1D1D] px-5 py-1.5 rounded-lg dark:text-[#A6A6A6]">
                            Software Developer </h3>
                        <div class="flex justify-center space-x-3">
                            <!-- facebook icon and link -->
                            <a href="https://www.facebook.com/" target="_blank" rel="noopener noreferrer">
                                <span class="socialbtn text-[#1773EA]">
                                    <i class="fa-brands fa-facebook-f"></i>
                                </span>
                            </a>
                            <!-- twitter icon and link -->
                            <a href="https://twitter.com/BrunoMugamba" target="_blank" rel="noopener noreferrer">
                                <span class="socialbtn text-[#1C9CEA]">
                                    <i class="fa-brands fa-twitter"></i>
                                </span>
                            </a>
                            <!-- dribbble icon and link -->
                            <a href="https://github.com/Mugamba669" target="_blank" rel="noopener noreferrer">
                                <span class="socialbtn dark:text-[#dddddd] text-[#000000]">
                                    <i class="fa-brands fa-github"></i>
                                </span>
                            </a>
                            <!-- linkedin icon and link -->
                            <a href="https://www.linkedin.com/" target="_blank" rel="noopener noreferrer">
                                <span class="socialbtn text-[#0072b1]">
                                    <i class="fa-brands fa-linkedin-in"></i>
                                </span>
                            </a>
                        </div>
                        <!-- personal infomation start -->
                        <div class="p-7 rounded-2xl mt-7 bg-[#F3F6F6] dark:bg-[#1D1D1D]">
                            <div class="flex border-b border-[#E3E3E3] dark:border-[#3D3A3A] pb-2.5">
                                <span class="socialbtn bg-white dark:bg-black text-[#E93B81] shadow-md">
                                    <i class="fa-solid fa-mobile-screen-button"></i>
                                </span>
                                <div class="text-left ml-2.5">
                                    <p class="text-xs text-[#44566C] dark:text-[#A6A6A6]"> Phone </p>
                                    <p class="dark:text-white">+256750482089</p>
                                </div>
                            </div>
                            <div class="flex border-b border-[#E3E3E3] dark:border-[#3D3A3A] py-2.5">
                                <span class="socialbtn bg-white dark:bg-black text-[#6AB5B9] shadow-md">
                                    <i class="fa-solid fa-envelope-open-text"></i>
                                </span>
                                <div class="text-left ml-2.5">
                                    <p class="text-xs text-[#44566C] dark:text-[#A6A6A6]"> Email </p>
                                    <a href="mailto:brunohectre@gmail.com" class="dark:text-white">brunohectre@gmail.com</a>
                                </div>
                            </div>
                            <div class="flex border-b border-[#E3E3E3] dark:border-[#3D3A3A] py-2.5">
                                <span class="socialbtn bg-white dark:bg-black text-[#FD7590] shadow-md">
                                    <i class="fa-solid fa-location-dot"></i>
                                </span>
                                <div class="text-left ml-2.5">
                                    <p class="text-xs text-[#44566C] dark:text-[#A6A6A6]"> Location </p>
                                    <p class="dark:text-white">Kampala</p>
                                </div>
                            </div>
                            <div class="flex py-2.5">
                                <span class="socialbtn bg-white dark:bg-black text-[#C17CEB] shadow-md">
                                    <i class="fa-solid fa-calendar-days"></i>
                                </span>
                                <div class="text-left ml-2.5">
                                    <p class="text-xs text-[#44566C] dark:text-[#A6A6A6]"> Birthday </p>
                                    <p class="dark:text-white">June 03, 2000</p>
                                </div>
                            </div>
                        </div>
                        <!-- personal infomation end-->
                        <!-- dowanload button -->
                        <button class="dowanload-btn">
                            <img class="mr-3" src="@/images/icons/dowanload.png" alt="icon" />
                                <a href="https://docs.google.com/document/d/1EwbVKJTqhBjSpgriCgzGLsTR2FWrpKFpWsLnQ1isoO0/view" download="Mugamba Bruno M.H">Download CV</a>
                             </button>
                    </div>
                </div>
            </div>
          
</template>
<script>
export default {
  name: "SideBar",
};
</script>
<style lang="">
</style>