<script>
import Menu from '../modal/Menu.vue';

export default {
    components: {
        Menu
    },
    data() {
        return {
            menu: false,
            bg: false

        }
    },
    methods: {
        barMenu() {
            this.menu = true;
            this.bg = true;
        },
        closeMenu(){
            this.menu = false;
            this.bg = false;
        }
    }
}

</script>


<template>
    <div class="fixed top-0 z-1000  w-full ">
        <div class=" flex  h-auto bg-blue-200 w-full justify-between   lg:px-25 md:px-0 sm:px-0">
            <div class="border w-70  border-hidden">
                <p class="lg:text-[8px] md:text-[10px] sm:text-[12px] text-white font-semibold py-1">CALL US NOW: +63917 883 3145</p>
            </div>
            <div class="flex gap-3">
                <p class="lg:text-[8px] md:text-[10px] sm:text-[12px] text-white font-semibold py-1">Log In/Register</p>
                <p class="lg:text-[8px] md:text-[10px] sm:text-[12px] text-white font-semibold py-1">My Acount.</p>
            </div>
        </div>
        <div
            class="flex justify-between items-center border-b-1 border-blue-500/20 w-full lg:px-25 md:px-10 sm:px-10 relative bg-white">
            <div class="shrink-0">
                <img class="h-20 w-20 rounded-full" src="../assets/images/logo-cleaning.jpeg" alt="">
            </div>
            <div class="flex  lg:flex md:flex sm:flex gap-3 justify-end font-bold lg:block md:block sm:hidden hidden cursor-pointer">
                <h1 class=" lg:text-[15px] md:text-[12px] sm:text-[10px] hover:bg-blue-100 px-2">Home</h1>
                <h1 class=" lg:text-[15px] md:text-[12px] sm:text-[10px]  hover:bg-blue-100 px-2">About Us</h1>
                <h1 class=" lg:text-[15px] md:text-[12px] sm:text-[10px]  hover:bg-blue-100 px-2">Services</h1>
                <h1 class=" lg:text-[15px] md:text-[12px] sm:text-[10px]  hover:bg-blue-100 px-2">Contact Us</h1>
                <h1 class=" lg:text-[15px] md:text-[12px] sm:text-[10px]  hover:bg-blue-100 px-2">FAQ</h1>
            </div>
            <div class="absolute right-35">
                <svg class="w-10 h-10 lg:hidden md:hidden sm:block " aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                    width="24" height="24" fill="none" viewBox="0 0 24 24" @click="barMenu()">
                    <path stroke="currentColor" stroke-linecap="round" stroke-width="2" d="M5 7h14M5 12h14M5 17h14" />
                </svg>

            </div>
            <div>
                <button
                    class="lg:text-[10px] md:text-[10px] sm:text-[8px] bg-blue-200 py-1 px-3 lg:px-2 md:px-2 sm:px-1 text-white rounded-full lg:font-bold md:font-bold sm:font-normal cursor-pointer">GET
                    A QOUTE</button>
            </div>
        </div>
    </div>
    <div class="w-full h-20">
        <h1></h1>
    </div>
    <!-- menu modal  -->
    <div v-if="menu" class="text-white h-auto w-40 bg-blue-200 text-2xl text-black shadow-2xl/20 text-center fixed right-48 top-20 z-4000 cursor-pointer font-bold">
        <h1 text-shadow-lg  >Home</h1>
        <h1 text-shadow-lg  >About Us</h1>
        <h1 text-shadow-lg >Services</h1>
        <h1 text-shadow-lg >Contact</h1>
        <h1 text-shadow-lg >FAQ</h1>
    </div>
    <div Menu @showThemenu="(closeMenu)" v-if="bg" @click="closeMenu" class="h-1100 w-full bg-white absolute top-0 z-3000 opacity-3 ">
    </div>
    
</template>