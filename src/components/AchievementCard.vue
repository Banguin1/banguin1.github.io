<template>
    <div
        class="relative flex gap-4 p-4 rounded-lg border-2 border-gray-800 w-80 lg:w-[600px] h-44 lg:h-[150px] bg-neutral-900/60">
        <img :src="image" alt="" class="w-14 h-14 rounded-lg" />
        <div class="flex flex-col gap-2">
            <div class="flex justify-between">
                <h3 class="font-bold text-neutral-300 text-sm lg:text-base">Spitzenreiter: {{ name }}</h3>
                <span class="text-sm lg:text-base">{{ date }}</span>
            </div>
            <span class="text-neutral-500 text-pretty text-xs lg:text-sm">Besiegt {{ location }} auf dem
                Schwierigkeitsgrad
                'Mythisch',
                bevor die nächste
                Schlachtzugsstufe veröffentlicht wird.</span>
        </div>
        <GlowingEffect :spread="20" :glow="true" :disabled="false" :proximity="300" :borderWidth="1" />
    </div>
</template>

<script setup lang="ts">
import GlowingEffect from './ui/glowing-effect/GlowingEffect.vue';

interface props {
    image: string;
    name: string;
    location: string;
    date: string;
}

const { image, name, location, date } = defineProps<props>();


</script>

<style scoped></style>