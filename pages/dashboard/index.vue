<template>
  <dashboard-layout>
    <template v-slot:content>
      <div
        class="
          w-full
          bg-white
          shadow
          text-gray-800
          grid grid-cols-3
          lg:px-80
          px-4
          items-center
          justify-center
          sticky
          top-0
        "
      >
        <div
          class="border-purple-700 hover:bg-gray-100 p-4 text-center cursor-pointer" :class="`${menu == 'home' && 'border-b-2'}`" @click="menu='home'"
        >
          <div class="font-bold text-purple-700"> Home </div>
        </div>
        <div class="border-purple-700 hover:bg-gray-100 p-4 text-center cursor-pointer" :class="`${menu == 'my-courses' && 'border-b-2'}`" @click="menu='my-courses'">
          <div class="font-bold text-purple-700"> My Courses </div>
        </div>
        <div class="border-purple-700 hover:bg-gray-100 p-4 text-center cursor-pointer" :class="`${menu == 'favorites' && 'border-b-2'}`" @click="menu='favorites'">
          <div class="font-bold text-purple-700"> Favorites </div>
        </div>
      </div>
      <div class="px-8 md:px-24">
        <section-home v-if="menu == 'home'"></section-home>
        <section-favorites v-if="menu == 'favorites'"></section-favorites>
        <section-my-courses v-if="menu == 'my-courses'"></section-my-courses>
      </div>
    </template>
  </dashboard-layout>
</template>

<script>
import DashboardLayout from "@/layouts/DashboardLayout.vue";
import SectionHome from "@/layouts/dashboard-sections/SectionHome.vue";
import SectionFavorites from "@/layouts/dashboard-sections/SectionFavorites.vue";
import SectionMyCourses from "@/layouts/dashboard-sections/SectionMyCourses.vue";
export default {
  components: { DashboardLayout, SectionHome, SectionFavorites, SectionMyCourses },
  name: "Dashbaord",
  data(){
    return {
      menu: "home",
    }
  }
};
</script>
