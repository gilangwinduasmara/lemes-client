<template>
  <div class="bg-white shadow">
    <div
      class="p-3 border-b flex justify-between hover:bg-gray-200 cursor-pointer"
      @click="expanded = !expanded"
    >
      <div>
        <slot name="header" />
      </div>
      <div class="">
        <unicon
          :class="`${expanded && 'rotate-180'}`"
          class="
            h-6
            w-6
            hover:bg-gray-100 hover:text-purple-500
            rounded-full
            cursor-pointer
            transition
            transform
            duration-700
            ease-in
          "
          name="angle-down"
          fill="currentColor"
        ></unicon>
      </div>
    </div>
    <div class="p-3" v-if="expanded">
      <slot name="content" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      expanded: false,
    };
  },
};
</script>