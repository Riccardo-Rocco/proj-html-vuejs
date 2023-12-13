<template>
    <div class="image-gallery">
        <div v-for="(item, index) in items" :key="index" class="gallery-item">
            <div class="overlay">
                <h2>{{ item.title }}</h2>
                <h4>{{ item.subtitle }}</h4>
                <button @click="handleButtonClick">{{ item.buttonText }}</button>
            </div>
            <img :src="item.image" alt="Gallery Image">
        </div>
    </div>
</template>
  
<script>
import WinterCollection from '../assets/images/winter_collection_bg.jpg';
import SpringCollection from '../assets/images/spring_collection_bg.jpg';
import AutumnCollection from '../assets/images/autumn_collection_bg.jpg';

export default {
    data() {
        return {
            items: [
                {
                    image: WinterCollection,
                    title: "Winter Collection",
                    subtitle: "STYLISH AND WARM",
                    buttonText: "VIEW MORE",
                },
                {
                    image: SpringCollection,
                    title: "Spring Collection",
                    subtitle: "BRIGHT AND COLORFUL",
                    buttonText: "VIEW MORE",
                },
                {
                    image: AutumnCollection,
                    title: "Autumn Collection",
                    subtitle: "RICH AND COMFORTABLE",
                    buttonText: "VIEW MORE",
                },
            ],
        };
    },
    methods: {
        handleButtonClick() {
            console.log('Hai cliccato su un pulsante nella galleria di immagini.');
        },
    },
};
</script>
  
  
<style scoped>
.image-gallery {
    display: flex;
    margin-top: 2rem;
}

.gallery-item {
    position: relative;
}

.gallery-item img {
    width: 100%;
    height: auto;
}

.overlay {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: #fff;
    width: 100%;
}

.overlay h2,
.overlay h4,
.overlay button {
    margin-bottom: 10px;
}

.overlay button {
    padding: 10px 20px;
    font-size: 1em;
    background-color: transparent;
    color: #fff;
    border: solid 1px white;
    border-radius: 20px;
    cursor: pointer;
}
</style>
  