<template>
    <div class="bg-gray-900 bg-opacity-50 w-screen h-screen absolute top-0 left-0 z-50" @click.self="$emit('close')">
        <div class="transition-all duration-500"></div>
        <transition
            enter-active-class="transition-all duration-500"
            enter-class="bg-red"
            enter-to-class="bg-white"
        >
            <div class="bg-white float-right h-full p-4 w-72 transition duration-500 transform" :class="profileWrapperClass">
                <div class="text-xl font-semibold">
                    Profile
                </div>
                <div class="mt-4 flex gap-2">
                    <div class="w-24 h-24 rounded-md bg-purple-200">

                    </div>
                    <div class="flex flex-col justify-between">
                        <div>
                            <div class="font-semibold">
                                Name
                            </div>
                            <div class="font-thin">
                                Student
                            </div>
                        </div>
                        <div class="font-thin">
                            <a href="/login" class="p-1 px-3 rounded-md text-white bg-purple-500">Logout</a>
                        </div>
                    </div>
                </div>
            </div>
        </transition>
    </div>
</template>

<script>
export default {
    data(){
        return {
            profileWrapperClass: 'translate-x-full'
        }
    },
    mounted(){
        this.$nextTick(function(){
            setTimeout(() => {
                this.profileWrapperClass = 'translate-x-0'
            },10)
        })
    },
}
</script>