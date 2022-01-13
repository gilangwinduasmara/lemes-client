<template>
  <div class="relative h-full">
    <div
      @click="$emit('close')"
      v-if="isOpen"
      class="
        w-screen
        h-screen
        fixed
        bg-gray-900
        top-0
        left-0
        z-50
        bg-opacity-75
        md:hidden
      "
    ></div>
    <div
      class="
        text-gray-100
        h-full
        transition-width
        transform
        duration-500
        overflow-x-hidden
        absolute
        md:relative
        z-50
      "
      :class="`${this.isOpen ? 'w-52' : 'w-0'}`"
    >
      <div class="bg-gray-9 h-full">
        <div class="w-52">
          <div class="p-4">
            <!-- Header -->
          </div>
          <div class="mt-8 p-2">
            <!-- <div class="bg-red-200 w-3 h-3"></div> -->
            <div href="/dashboard" class="">
              <div
                class="
                  px-4
                  py-2
                  flex
                  gap-4
                  items-center
                  hover:bg-gray-7
                  rounded-md
                  cursor-pointer
                  transition-colors
                "
              >
                <div class="h-4 w-4 bg-blue-200 rounded"></div>
                <div>Dashboard</div>
              </div>
            </div>
            <div
              class="
                px-4
                py-2
                hover:bg-gray-7
                rounded-md
                cursor-pointer
                flex
                gap-4
                items-center
                transition-colors
              "
            >
              <div class="h-4 w-4 bg-blue-200 rounded"></div>
              <div>Certificates</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['isOpen'],
  data() {
    return {
      //   wrapperWidthClass: "w-0",
    }
  },
  mounted() {},
}
</script>
