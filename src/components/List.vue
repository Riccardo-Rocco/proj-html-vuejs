<template>
    <div class="component-container">
        <div v-for="(list, index) in lists" :key="index" class="list">
            <h4>{{ list.title }}</h4>
            <div v-for="card in list.cards" :key="card.id" class="card mb-3" style="max-width: 540px;">
                <div class="row g-0">
                    <div class="col-md-4">
                        <img :src="card.image" class="img-fluid rounded-start" alt="Card Image">
                    </div>
                    <div class="col-md-8">
                        <div class="card-body">
                            <h6 class="card-title">{{ card.name }}</h6>
                            <div class="rating">
                                <span v-for="star in card.stars" :key="star" class="star">&#9733;</span>
                            </div>
                            <p class="card-text"><small class="text-muted">Price: {{ card.price }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>
import Prodotto1 from "../assets/images/black_leather_jacket-120x156.jpg";
import Prodotto2 from "../assets/images/black_elegant_leather_jacket-120x156.jpg";
import Prodotto3 from "../assets/images/hipster_black_top-120x156.jpg";
import Prodotto4 from "../assets/images/blue_leather_jacket-120x156.jpg";
import Prodotto5 from "../assets/images/spring_printed_dress-120x156.jpg";
import Prodotto6 from "../assets/images/leather_gloves-120x156.jpg";

export default {
    data() {
        return {
            lists: [
                {
                    title: "FEATURED",
                    cards: [
                        { id: 1, name: "Black Jacket", stars: 4, price: "$50.00", image: Prodotto1 },
                        { id: 2, name: "Black Leather Jacket", stars: 5, price: "$30.00", image: Prodotto2 },
                        { id: 3, name: "Hipster Black Top ", stars: 3, price: "$45.00", image: Prodotto3 },
                    ],
                },
                {
                    title: "ON SALE",
                    cards: [
                        { id: 1, name: "Blue Leather Jacket", stars: 4, price: "$50.00", image: Prodotto4 },
                        { id: 2, name: "Black Leather Jacket", stars: 5, price: "$30.00", image: Prodotto2 },
                        { id: 3, name: "Spring Printed Dress", stars: 3, price: "$45.00", image: Prodotto5 },
                    ],
                },
                {
                    title: "TOP RATED",
                    cards: [
                        { id: 1, name: "Spring Printed Dress", stars: 4, price: "$50.00", image: Prodotto5 },
                        { id: 2, name: "Leather Gloves", stars: 5, price: "$30.00", image: Prodotto6 },
                        { id: 3, name: "Black Leather Jacket", stars: 3, price: "$45.00", image: Prodotto2 },
                    ],
                },
                {
                    title: "LATEST REVIEWS",
                    cards: [
                        { id: 1, name: "Black Leather Jacket", stars: 4, price: "$50.00", image: Prodotto2 },
                        { id: 2, name: "Leather Gloves", stars: 5, price: "$30.00", image: Prodotto6 },
                        { id: 3, name: "Spring Printed Dress", stars: 3, price: "$45.00", image: Prodotto5 },
                    ],
                },
            ],
        };
    },
};
</script>
  
<style scoped>
.component-container {
    display: flex;
    justify-content: center;
    margin-top: 10%;
}

.list {
    width: 20%;
    text-align: center;
    margin: 10px;
}

.card {
    margin-bottom: 20px;
    padding: 10px;
    border: none;
    background: #fff;
    position: relative;
}
</style>
  