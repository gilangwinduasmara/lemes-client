<template>
  <div
    class="flex justify-between text-cyan-300 p-4 items-center z-50 bg-white"
  >
    <div class="flex items-center gap-4">
      <div
        class="flex flex-col gap-1 cursor-pointer hover:shadow-md p-2 rounded"
        @click="$emit('burgerClick')"
      >
        <div
          class="
            bg-gray-900
            rounded
            h-0.5
            w-5
            transform
            delay-500
            ease-out
            duration-500
          "
          :class="`${
            isSideMenuOpen ? '-rotate-45 translate-y-1.5' : ''
          }`"
        ></div>
        <div
          class="
            bg-gray-900
            rounded
            h-0.5
            w-5
            transform
            delay-500
            ease-out
            duration-500
            origin-right
          "
          :class="`${isSideMenuOpen && 'scale-x-0 '}`"
        ></div>
        <div
          class="
            bg-gray-900
            rounded
            h-0.5
            w-5
            transform
            delay-500
            ease-out
            duration-500
          "
          :class="`${
            isSideMenuOpen ? 'rotate-45 -translate-y-1.5' : ''
          }`"
        ></div>
      </div>
      <div class="hidden md:block">
        <div class="text-3xl font-bold text-purple-900">Lemes</div>
        <div class="text-xs text-purple-500">Learning Management System</div>
      </div>
    </div>
    <div class="flex relative flex-grow justify-end md:justify-center mr-2">
      <input
        @focus="isSearchFocus = true"
        @blur="isSearchFocus = false"
        type="text"
        class="shadow-md p-2 px-4 rounded-xl outline-none transition-width duration-700"
        :class="`${isSearchFocus ? 'w-5/6 md:w-1/3' : 'w-7/12 md:w-1/3'}`"
        placeholder="Search"
        @input="onSearchChange"
      />
      <div
        class="
          absolute
          -bottom-14
          bg-white
          z-50
          rounded-md
          shadow-lg
          w-full
          p-2
        "
        v-if="search"
      >
        a
      </div>
    </div>
    <div
      class="
        flex
        gap-2
        items-center
        cursor-pointer
        hover:bg-gray-100
        rounded-md
        p-2
        px-4
      "
      @click="openProfile"
    >
      <div class="h-8 w-8 bg-gray-600 rounded-full"></div>
      <div class="hidden md:block">Profile</div>
    </div>
    <side-profile v-if="showProfile" @close="hideProfile"></side-profile>
  </div>
</template>

<script>
import SideProfile from "./SideProfile.vue";
export default {
  components: { SideProfile },
  props: ["isSideMenuOpen"],
  data() {
    return {
      showProfile: false,
      search: "",
      isSearchFocus: false,
    };
  },
  methods: {
    openProfile: function () {
      this.showProfile = true;
    },
    hideProfile: function () {
      this.showProfile = false;
    },
    onSearchChange: function (event) {
      console.log(event.target.value);
      this.search = event.target.value;
    },
  },
};
</script>
