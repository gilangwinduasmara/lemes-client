<template>
  <div class="overflow-hidden max-h-screen bg-gray-50">
    <div class="flex">
      <div class="h-screen">
        <side-menu @close="isSideMenuOpen=false" :isOpen="isSideMenuOpen"></side-menu>
      </div>
      <div class="flex-grow">
        <navigation
          @burgerClick="isSideMenuOpen = !isSideMenuOpen"
          :isSideMenuOpen="isSideMenuOpen"
        ></navigation>
        <div class="h-screen overflow-y-scroll pb-28 relative">
          <div
            class="
              w-full
              bg-gradient-to-r
              from-blue-600
              to-blue-400
              p-4
              text-white
              flex
              items-center
              justify-center
              gap-3
              relative
              flex-col
              md:flex-row
            "
            v-if="isPromotionShow"
          >
            <div class="font-bold">Limited Offer! </div>
            <div>
              Get Promager Academy Unlimited for just Rp 50.000,00/month if you
              are a student.
            </div>
            <div>
              <div
                class="
                  p-1
                  px-3
                  border-white
                  hover:bg-white hover:text-blue-400
                  border-2
                  cursor-pointer
                  transition-all
                  duration-200
                "
              >
                Get Unlimited
              </div>
            </div>
            <div class="absolute top-4 md:top-auto right-0 pr-4">
              <div
                @click="isPromotionShow = false"
                class="
                  text-white
                  cursor-pointer
                  rounded-full
                  hover:shadow hover:bg-white hover:text-blue-400
                  h-6
                  w-6
                  flex
                  items-center
                  justify-center
                  transition
                "
              >
                <unicon name="times" fill="currentColor"></unicon>
              </div>
            </div>
          </div>

          <div class="min-h-full  top-0">
            <slot name="content" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Navigation from "@/components/Navigation.vue";
import SideMenu from "@/components/SideMenu.vue";
export default {
  components: {
    Navigation,
    SideMenu,
  },
  data() {
    return {
      isSideMenuOpen: true,
      isPromotionShow: true,
    };
  },
};
</script>
