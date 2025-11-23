<template>
    <div class="relative w-5/6 mx-auto">
        <div
            class="absolute left-0 top-0 bottom-0 w-60 bg-linear-to-r from-background to-transparent z-10 pointer-events-none">
        </div>
        <div
            class="absolute right-0 top-0 bottom-0 w-60 bg-linear-to-l from-background to-transparent z-10 pointer-events-none">
        </div>
        <Marquee class="[--duration:120s]">
            <AchievementCard v-for="achievement in firstFive" :key="achievement.id" :image="achievement.image"
                :name="achievement.name" :location="achievement.location" :date="achievement.date" />
        </Marquee>
        <Marquee class="[--duration:120s]" :reverse="true">
            <AchievementCard v-for="achievement in lastFive" :key="achievement.id" :image="achievement.image"
                :name="achievement.name" :location="achievement.location" :date="achievement.date" />
        </Marquee>
    </div>
</template>

<script setup lang="ts">
import AchievementCard from '@/components/AchievementCard.vue';
import Marquee from '@/components/ui/marquee/Marquee.vue';
import cuttingEdge from '@/assets/cutting-edge.json';

// Dynamisch Bilder importieren
const getImageUrl = (imageName: string) => {
    return new URL(`../../../assets/av-icons/${imageName}`, import.meta.url).href;
};

const achievements = Object.values(cuttingEdge).map((achievement: any) => ({
    ...achievement,
    image: getImageUrl(achievement.image)
}));

const firstFive = achievements.slice(0, 5);
const lastFive = achievements.slice(-5);
</script>

<style scoped></style>