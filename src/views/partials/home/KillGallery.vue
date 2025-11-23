<template>
    <div class="kill-gallery-section py-32">
        <div class="container flex flex-col items-center">
            <h2 class="flex justify-center text-4xl lg:text-5xl md:text-6xl font-bold mb-10">
                <span class="bg-linear-to-r from-[#ff4757] to-[#80af13] bg-clip-text text-transparent">
                    Ein Team. Ein Ziel.
                </span>
            </h2>
            <Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true"
                :showItemNavigators="true" :showThumbnails="true" :showThumbnailNavigators="false"
                containerStyle="max-width: 90%" class="mx-auto custom-galleria" :pt="{
                    root: {
                        class: 'border-neutral-700!'
                    },
                    thumbnailContent: {
                        class: 'bg-black!'
                    }
                }">
                <template #item="slotProps">
                    <div class="gallery-item-wrapper">
                        <img :src="slotProps.item.src" :alt="slotProps.item.alt" class="gallery-image" />
                    </div>
                </template>
                <template #thumbnail="slotProps">
                    <img :src="slotProps.item.src" :alt="slotProps.item.alt" class="thumbnail-image" />
                </template>
            </Galleria>
        </div>
    </div>
</template>

<script setup lang="ts">
import Galleria from 'primevue/galleria';

const images = [
    {
        src: new URL('@/assets/images/dimensius-kill.webp', import.meta.url).href,
        alt: 'Dimensius Kill'
    },
    {
        src: new URL('@/assets/images/gallywix-kill.webp', import.meta.url).href,
        alt: 'Gallywix Kill'
    },
    {
        src: new URL('@/assets/images/ansurek-kill.webp', import.meta.url).href,
        alt: 'Ansurek Kill'
    },
    {
        src: new URL('@/assets/images/fyrakk-kill.webp', import.meta.url).href,
        alt: 'Fyrakk Kill'
    },
    {
        src: new URL('@/assets/images/sarkareth-kill.webp', import.meta.url).href,
        alt: 'Sarkareth Kill'
    },
    {
        src: new URL('@/assets/images/raszageth-kill.webp', import.meta.url).href,
        alt: 'Raszageth Kill'
    },
    {
        src: new URL('@/assets/images/jailer-kill.webp', import.meta.url).href,
        alt: 'Jailer Kill'
    },
    {
        src: new URL('@/assets/images/sylvanas-kill.webp', import.meta.url).href,
        alt: 'Sylvanas Kill'
    },
    {
        src: new URL('@/assets/images/denathrius-kill.webp', import.meta.url).href,
        alt: 'Denathrius Kill'
    }
];

const responsiveOptions = [
    {
        breakpoint: '1024px',
        numVisible: 5
    },
    {
        breakpoint: '768px',
        numVisible: 3
    },
    {
        breakpoint: '560px',
        numVisible: 1
    }
];
</script>

<style scoped>
/* Wrapper für zentrierte Bilder */
.gallery-item-wrapper {
    width: 100%;
    height: 600px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #000000;
}

/* Hauptbild - immer gleiche Höhe, optimal angepasst */
.gallery-image {
    max-height: 600px;
    max-width: 100%;
    height: 600px;
    width: auto;
    object-fit: contain;
    display: block;
}

.thumbnail-image {
    width: 100%;
    height: 80px;
    object-fit: cover;
    display: block;
}

/* Responsive Anpassungen */
@media (max-width: 768px) {
    .gallery-item-wrapper {
        height: 400px;
    }

    .gallery-image {
        max-height: 400px;
        height: 400px;
    }

    .thumbnail-image {
        height: 60px;
    }
}

@media (max-width: 480px) {
    .gallery-item-wrapper {
        height: 300px;
    }

    .gallery-image {
        max-height: 300px;
        height: 300px;
    }
}
</style>
