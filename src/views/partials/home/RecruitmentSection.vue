<template>
    <div class="relative w-full overflow-hidden py-32">

        <!-- Boss Images - Left Side (Void/Leere) -->
        <div v-animateonscroll="{ enterClass: 'animate-fade-in-left' }"
            class="absolute left-0 top-76 lg:top-32 w-1/2 lg:w-1/4">
            <!-- Void Glow Effect -->
            <div class="absolute inset-0 blur-[100px] opacity-60 -translate-x-40 lg:translate-x-0">
                <div class="absolute top-1/4 left-1/4 w-64 h-64 bg-purple-600 rounded-full"></div>
                <div class="absolute top-1/2 left-1/3 w-80 h-80 bg-blue-900 rounded-full"></div>
                <div class="absolute top-1/3 left-1/2 w-48 h-48 bg-indigo-800 rounded-full"></div>
            </div>
            <img src="../../../assets/images/clash-dark.webp" alt="Raid Boss" class="relative z-10 w-[500px] h-auto" />
        </div>

        <!-- Boss Images - Right Side (Light/Licht) -->
        <div v-animateonscroll="{ enterClass: 'animate-fade-in-right' }"
            class="absolute right-0 top-82 lg:top-72 w-1/2 lg:w-1/3">
            <!-- Light Glow Effect -->
            <div class="absolute inset-0 blur-[100px] opacity-60 translate-x-80 lg:translate-x-0 -translate-y-20">
                <div class="absolute top-1/4 right-1/4 w-64 h-64 bg-yellow-400 rounded-full"></div>
                <div class="absolute top-1/2 right-1/3 w-80 h-80 bg-amber-500 rounded-full"></div>
                <div class="absolute top-1/3 right-1/2 w-48 h-48 bg-orange-400 rounded-full"></div>
            </div>
            <img src="../../../assets/images/clash-light.webp" alt="Raid Boss" class="relative z-10 w-full h-auto" />
        </div>

        <!-- Content -->
        <div class="relative z-10 container mx-auto px-6">
            <div class="max-w-3xl mx-auto text-center">
                <!-- Headline -->
                <h2 class="text-5xl md:text-6xl font-bold mb-4">
                    <span class="bg-linear-to-r from-[#9333ea] to-[#f59e0b] bg-clip-text text-transparent">
                        Bereit für Progress?
                    </span>
                </h2>
                <p
                    class="text-xl p-2 bg-neutral-900/50 rounded-lg lg:bg-transparent lg:p-0 text-neutral-100 lg:text-neutral-400 mb-16">
                    Wir suchen motivierte Raider für unseren Mythic Kader
                </p>

                <!-- Two Column Layout -->
                <div class="grid md:grid-cols-2 gap-12 mb-16 mt-40 lg:mt-0">
                    <!-- Was wir erwarten -->
                    <div class="bg-neutral-900/50 backdrop-blur-sm rounded-lg p-8 border border-neutral-800">
                        <h3 class="text-2xl font-bold text-[#9333ea] mb-6 flex items-center justify-center gap-2">
                            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                            Was wir erwarten
                        </h3>
                        <ul class="text-left space-y-3 text-neutral-300">
                            <li class="flex items-center gap-3">
                                <span class="text-[#9333ea] mt-1">▸</span>
                                <span>85%+ Raidanwesenheit</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <span class="text-[#9333ea] mt-1">▸</span>
                                <span>Aktives Gameplay außerhalb der Raids</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <span class="text-[#9333ea] mt-1">▸</span>
                                <span>Klassenverständnis und Flexibilität</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <span class="text-[#9333ea] mt-1">▸</span>
                                <span>Eigenständige Vorbereitung</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <span class="text-[#9333ea] mt-1">▸</span>
                                <span>Teamfähigkeit & Kommunikation</span>
                            </li>
                        </ul>
                    </div>

                    <!-- Was wir bieten -->
                    <div class="bg-neutral-900/50 backdrop-blur-sm rounded-lg p-8 border border-neutral-800">
                        <h3 class="text-2xl font-bold text-[#f59e0b] mb-6 flex items-center justify-center gap-2">
                            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
                            </svg>
                            Was wir bieten
                        </h3>
                        <ul class="text-left space-y-3 text-neutral-300">
                            <li class="flex items-center gap-3">
                                <span class="text-[#f59e0b] mt-1">▸</span>
                                <span>Strukturierte Raids</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <span class="text-[#f59e0b] mt-1">▸</span>
                                <span>Erfahrene Raidleitung</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <span class="text-[#f59e0b] mt-1">▸</span>
                                <span>Freundliche & respektvolle Community</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <span class="text-[#f59e0b] mt-1">▸</span>
                                <span>Erfolgreiche Progress-Geschichte</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <span class="text-[#f59e0b] mt-1">▸</span>
                                <span>M+ Gruppen & andere Aktivitäten</span>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Contact Section -->
                <div class="bg-neutral-900/50 backdrop-blur-sm rounded-lg p-8 border border-neutral-700">
                    <h3 class="text-xl text-neutral-200 mb-6">Interesse geweckt?</h3>
                    <div class="flex flex-col lg:flex-row items-center justify-center gap-4 lg:gap-20">
                        <div class="flex items-center gap-4">
                            <MdiBattlenet class="w-12 h-12 text-[#1690ff]" />
                            <span class="font-bold text-3xl">Scathyo#2492</span>
                        </div>
                        <div class="flex items-center gap-4">
                            <MdiBattlenet class="w-12 h-12 text-[#1690ff]" />
                            <span class="font-bold text-3xl">Banguin#2457</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import MdiBattlenet from '~icons/mdi/battlenet'

</script>

<style scoped>
@keyframes fade-in-left {
    from {
        opacity: 0;
        transform: translateX(-100%);
    }

    to {
        opacity: 1;
        transform: translateX(0);
    }
}

@keyframes fade-in-right {
    from {
        opacity: 0;
        transform: translateX(100%);
    }

    to {
        opacity: 1;
        transform: translateX(0);
    }
}

.animate-fade-in-left {
    animation: fade-in-left 1s ease-out forwards;
}

.animate-fade-in-right {
    animation: fade-in-right 1s ease-out forwards;
}
</style>
