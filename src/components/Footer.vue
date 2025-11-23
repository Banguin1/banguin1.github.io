<template>
    <footer class="w-full border-t border-neutral-800 bg-neutral-950/50 backdrop-blur-sm">
        <div class="container mx-auto px-6 py-8">
            <div class="flex flex-col md:flex-row justify-between items-center gap-6">
                <!-- Guild Info -->
                <div class="flex flex-col items-center md:items-start">
                    <img src="../assets/images/xore.webp" alt="Xore Logo" class="w-14 h-14">
                </div>

                <!-- Links -->
                <div class="flex flex-col lg:flex-row items-center gap-8 lg:gap-20">
                    <a href="https://www.wowprogress.com/guild/eu/eredar/Xore" target="_blank"
                        class="flex items-center gap-2">
                        <img src="../assets/images/wowprogress.webp" alt="Wowprogress Badge" class="h-8 w-8" />
                        <span>wowprogress</span>
                    </a>
                    <a href="https://raider.io/guilds/eu/eredar/Xore" target="_blank" class="flex items-center gap-2">
                        <img src="../assets/images/raiderio.webp" alt="Raider.io Badge" class="h-8 w-8" />
                        <span>raider.io</span>
                    </a>
                    <a href="https://www.warcraftlogs.com/guild/id/320951" target="_blank"
                        class="flex items-center gap-2">
                        <img src="../assets/images/wowlogs.webp" alt="Warcraft Logs Badge" class="h-8 w-8" />
                        <span>warcraft logs</span>
                    </a>
                </div>

                <!-- Copyright -->
                <div class="text-center md:text-right">
                    <p @click="router.push('/uschi')" class="text-xs text-neutral-500">
                        © {{ currentYear }} Xore. All rights reserved.
                    </p>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup lang="ts">
import { useRouter } from 'vue-router';


const router = useRouter();
const currentYear = new Date().getFullYear();
</script>

<style scoped></style>
