<template>
  <div class="relative" @mouseover="hover = true" @mouseleave="hover = false">
    <img :src="src" alt="" class="rounded-lg w-full h-full">
    <div v-if="hover" class="absolute bg-black opacity-50 inset-0 w-full h-full rounded-lg"></div>
    <div v-if="hover" class="absolute top-0 w-full h-full flex flex-col justify-between p-2">
        <div class="flex items-center justify-between">
            <button type="button" name="button" class="flex items-center">
            </button>
            <button type="button" name="button" class="rounded-full p-2 text-white bg-red-500 font-semibold text-sm">Save</button>
        </div>
        <div class="flex items-center w-full">
            <button type="button" name="button" class="ml-auto mr-2 bg-white rounded-full w-8 h-8 flex items-center justify-center text-black-100 opacity-75 hover:opacity-100">
                <span class="material-icons w-6">ios_shared</span>
            </button>
            <button type="button" name="button" class="bg-white rounded-full w-8 h-8 flex items-center justify-center text-black-100 opacity-75 hover:opacity-100">
                <span class="material-icons text-base">more_horiz</span>
            </button>
        </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
    props:['src'],
    setup(){
        let hover = ref(false)
        return {
            hover
        }
    }
}
</script>

<style>

</style>