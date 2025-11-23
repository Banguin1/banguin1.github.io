<template>
    <div class="h-dvh w-full flex items-center justify-center relative">
        <div class="flex items-center justify-between w-1/2 h-full">
            <div class="flex flex-col text-3xl z-10">
                <span class="text-neutral-400">
                    Deine World of Warcraft Community
                </span>
                <div>
                    <span class="text-neutral-400">
                        für
                    </span>
                    <span class="inline-flex justify-centermin-w-[200px] w-[200px]">
                        <FlipWords :words="bannerFlipWords" class="text-neutral-300 font-bold" />
                    </span>
                    <span class="text-neutral-400">
                        Progress
                    </span>
                </div>
            </div>
            <div class="flex flex-col  items-center z-10">
                <h1 class="text-9xl font-bold bg-linear-to-r from-[#ff4757] to-[#80af13] bg-clip-text text-transparent">
                    Xore
                </h1>
                <span class="text-2xl text-neutral-400">EU - Eredar</span>
            </div>
        </div>
        <div class="absolute bottom-1 animate-bounce flex flex-col items-center justify-center z-10 transition-opacity duration-500"
            :style="{ opacity: scrollIndicatorOpacity }">
            <MdiArrowDown class="w-8 h-8 text-white" />
        </div>
        <BgNeural :hue="310" :chroma="0.4" class="opacity-50" />
    </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
import BgNeural from '@/components/ui/bg-neural/NeuralBg.vue'
import FlipWords from '@/components/ui/flip-words/FlipWords.vue';
import MdiArrowDown from '~icons/mdi/arrow-down';

const bannerFlipWords = [
    'respektvollen',
    'organisierten',
    'erfolgreichen',
]

const scrollIndicatorOpacity = ref(0.3)

const handleScroll = () => {
    const scrolled = window.scrollY
    const maxScroll = 200
    const opacity = Math.max(0, 0.3 - (scrolled / maxScroll) * 0.3)
    scrollIndicatorOpacity.value = opacity
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped></style>