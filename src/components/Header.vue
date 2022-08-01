<template>
    <div class="px-3 py-4 flex items-center justify-between w-full">
        <div class="flex items-center">
            <button class="rounded-full hover:bg-gray-100 p-3 flex items-center justify-center" type="button" name="button">
                <img src="../assets/logo.png" alt="logo" class="h-6 w-6">
            </button>
            <button  v-for="tabItem in tabItems" :key="tabItem" @click="selectedTab = tabItem.key" type="button" name="button" :class="`${selectedTab === tabItem.key ? 'bg-black text-white' : 'text-black hover:bg-gray-100'} rounded-full py-3 px-4 font-semibold`">{{tabItem.name}}</button>
        </div>
        
        <div class="flex-grow relative">
            <span class="material-icons absolute mt-3 ml-3 text-muted">search</span>
            <input class="w-full hoer:bg-lightHover rounded-full bg-light py-3 pr-3 pl-10" type="text" placeholder="Search">
        </div>

        <div class="flex items-center">
            <button class="relative rounded-full hover:bg-gray-100 flex items-center justify-center p-3" type="button" name="button">
                <span class="material-icons text-3xl text-muted">notifications</span>
                <div class="rounded-full h-4 w-4 bg-red-500  text-sm text-white flex items-center justify-center absolute mb-5 ml-5">4</div>
            </button>
            <button class="relative rounded-full hover:bg-gray-100 flex items-center justify-center p-3" type="button" name="button">
                <span class="material-icons text-3xl text-muted">textsms</span>
                <div class="rounded-full h-4 w-4 bg-red-500 text-sm text-white flex items-center justify-center absolute mb-5 ml-5">4</div>
            </button>
            <button class="rounded-full hover:bg-gray-100 p-3 flex items-center justify-center" type="button" name="button">
                <img src="../assets/profile.jpg" alt="profile" class="h-8 w-8 rounded-full">
            </button>
            <button class="w-6 h-6 hover:bg-gray-100 rounded-full items-center justify-center" type="button" name="button"><span class="material-icons text-3xl text-muted">expand_more</span>
            </button>
        </div>
    </div>
</template>

<script>
export default {
    setup(){
        return{
            tabItems:[
                {name:'Home', key:'home'},
                {name:'Today', key:'today'}
            ],
            selectedTab: 'home'
        }
    }
}
</script>

<style>

</style>