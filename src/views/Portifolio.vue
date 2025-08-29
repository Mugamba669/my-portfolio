<template>
  <layout title="My Works">
    <section id="portfolio" class="bg-white lg:rounded-2xl dark:bg-[#111111]">
      <div class="container mb-8 px-4 sm:px-5 md:px-10 lg:px-[60px]">
        <!-- responsive navigator -->
        <div class="py-12">
          <h1 class="after-effect after:left-48 lg:mt-0">My Work</h1>

          <ul
            class="button-group isotop-menu-wrapper mt-[30px] flex w-full justify-start md:justify-end flex-wrap font-medium"
          >
            <li
              :class="[
                type == 'all' ? 'is-checked' : '',
                'fillter-btn mr-4 md:mx-4',
              ]"
              data-filter="*"
              @click="all()"
            >
              All
            </li>
            <li
              :class="[
                type == 'mobile' ? 'is-checked' : '',
                'fillter-btn mr-4 md:mx-4',
              ]"
              @click="mobile()"
              data-filter=".dev"
            >
              Mobile Apps
            </li>
            <li
              :class="[
                type == 'web' ? 'is-checked' : '',
                'fillter-btn mr-4 md:mx-4',
              ]"
              @click="web()"
              data-filter=".plugin"
            >
              Web Design
            </li>
            <li
              :class="[
                type == 'desktop' ? 'is-checked' : '',
                'fillter-btn mr-4 md:mx-4',
              ]"
              @click="desktop()"
              data-filter=".branding"
            >
              Desktop
            </li>
          </ul>
        </div>
        <!-- <div id="" class="mymix portfolio_list-two two-col"> -->
        <!-- <div class="grid-sizer"> -->
        <transition name="fade">
          <work-card
            class="display-grid"
            :works="type == '' ? items : items.filter((x) => x.type == type)"
          />
        </transition>
      </div>
    </section>
  </layout>
</template>

<script>
import Layout from "@/Layout/layout.vue";
import WorkCard from "@/components/works/WorkCard.vue";
export default {
  name: "Portfolio",
  data() {
    return {
      type: "",
      items: [
        {
          name: "Skooltym Admin",
          type: "web",
          link: "http://skooltym.com/",
          img: "https://play-lh.googleusercontent.com/TmZYBIRpnB5cEE4R9uVOBZymWUALAi2W8QWL2It_wV020Drc6y_ToNlg-fSiUIaTdg=w1052-h592-rw",
        },
        {
          name: "Hype Muzik Web Version",
          type: "web",
          link: "https://hype-muzik.netlify.app/",
          img: "https://avatars.githubusercontent.com/u/61741704?v=4",
        },
        {
          name: "Tasye Ecom - E-commerce Platform (Uganda)",
          type: "web",
          link: "https://tasye.com/",
          img: require("@/images/work_images/tasy.png"),
        },
        {
          name: "Aisiom - E-learning Platform (East Africa)",
          type: "web",
          link: "https://brunokabugo.com/",
          img: require("@/images/work_images/asomata.png"),
        },
        {
          name: "COTE - Enterprise Website (Next.js - Uganda)",
          type: "web",
          link: "https://coteug.com/",
          img: require("@/images/work_images/cote.png"),
        },
        {
          name: "COTE Rentals - Property Management Platform (Uganda)",
          type: "web",
          link: "https://rentals.coteug.com",
          img: require("@/images/work_images/rental.png"),
        },
        {
          name: "LW Amp - Desktop Music Player (Ubuntu/Linux)",
          type: "desktop",
          link: "https://snapcraft.io/lw-ziki-amp",
          img: "https://res.cloudinary.com/canonical/image/fetch/f_auto,q_auto,fl_sanitize,w_819,h_460/https://dashboard.snapcraft.io/site_media/appmedia/2021/10/Screenshot_from_2021-10-04_19-39-35_Vfk4oaZ.png",
        },
        {
          name: "Hype Muzik - Music Streaming App (Android - Uganda)",
          type: "mobile",
          link: "https://play.google.com/store/apps/details?id=x.a.zix",
          img: "https://play-lh.googleusercontent.com/zhUJ3yMxBy6RIpmz0rF5L1vF5warWLLvgzLvRiMre9M7GoE1PkuIbN6MyVRISZBrgP3s=w1052-h592-rw",
        },
        {
          name: "Planar - Personal Finance Tracker (Android - Uganda)",
          type: "mobile",
          link: "https://play.google.com/store/apps/details?id=com.app.tenant",
          img: "https://play-lh.googleusercontent.com/zAcwmOJoSk3NB-l5p7VdbouopaNFM1cIqy8rfwWXYJ-nJl2pOhjXIVAHHAlBqA_-nkLr1F3hkWnc-yxvPxxaV6E=w5120-h2880-rw",
        },
        {
          name: "Skooltym - School Management System (Android - Uganda)",
          type: "mobile",
          link: "https://play.google.com/store/apps/details?id=app.malticard.skool_tym",
          img: "https://play-lh.googleusercontent.com/Mews0pKfMv7cgopRgTXphtAXcWN9uLdjPcl9s_pVH_Wes0IWDWXr4U6mkccuVxV1hec=w832-h470-rw",
        },
      ],
    };
  },
  methods: {
    all() {
      this.type = "";
    },
    mobile() {
      this.type = "mobile";
    },
    web() {
      this.type = "web";
    },
    desktop() {
      this.type = "desktop";
      console.log(this.type);
    },
  },
  components: {
    Layout,
    WorkCard,
  },
};
</script>

<style lang="scss" scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.display-grid {
  width: 100% !important;
  border-radius: 10px;
  padding: 10px;
  height: 100%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 20px;
  grid-auto-rows: 1fr;
  grid-auto-flow: dense;
  div {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
  }
}

@media (max-width: 768px) {
  .display-grid {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 15px;
    padding: 5px;
  }
}

@media (max-width: 640px) {
  .display-grid {
    grid-template-columns: 1fr;
    grid-gap: 10px;
    padding: 5px;
  }
}
// @media (min-width: 768px) {
//   .display-grid {
//     width: 100% !important;
//     border-radius: 10px;
//     padding: 10px;
//     height: 100%;
//     display: grid;
//     grid-template-columns: repeat(2, 1fr);
//     grid-gap: 20px;
//     grid-auto-rows: minmax(100px, auto);
//     grid-auto-flow: dense;
//     div {
//       width: 100%;
//       height: 100%;
//     }
//   }
// }
// @media (min-width: 640px) {
//   .display-grid {
//     width: 100% !important;
//     border-radius: 10px;
//     padding: 10px;
//     height: 100%;
//     display: grid;
//     grid-template-columns: repeat(1, 1fr);
//     grid-gap: 20px;
//     grid-auto-rows: minmax(100px, auto);
//     grid-auto-flow: dense;
//     div {
//       width: 100%;
//       height: 100%;
//     }
//   }
// }
</style>
