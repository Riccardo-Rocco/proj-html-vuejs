<template>
  <div>
    <!--titolo-->
    <div class="shop-container">
      <h1>Featured Products</h1>
      <h4>Must have products from our top sellers</h4>

    </div>

    <!--sezione menu scelta categoria-->
    <div class="menu">
      <button v-for="category in categories" :key="category.name" @click="changeCategory(category)">
        {{ category.name }}
      </button>
    </div>
    <!--funzione per popolare le cards-->
    <div class="cards">
      <div v-for="card in activeCategory.cards" :key="card.id" class="card">
        <img :src="card.image" alt="Product Image" @mouseover="showCardOptions(card.id)">
        <div class="info">
          <h5>{{ card.title }}</h5>
          <h6><a :href="`#${card.id}`">{{ card.subtitle }}</a></h6>
          <p>
            <span v-if="card.discountPrice" class="original-price">{{ card.originalPrice }}</span>
            {{ card.price }}
          </p>
        </div>
        <div v-if="cardOptions[card.id]" class="card-options">
          <a @click="addToCart(card.id)"><i class="fas fa-cart-shopping">Add to Cart</i></a>
          <a @click="showDetails(card.id)"><i class="fas fa-bars">Details</i></a>
        </div>
      </div>
    </div>
  </div>
</template>
  
<script>
import '@fortawesome/fontawesome-free/css/all.css';//import fontawesome
//import imagini come modulo 
import ElegantImage from '../assets/images/black_elegant_leather_jacket.jpg';
import BlackLeatherSuitImage from '../assets/images/black_leather_suit.jpg';
import BlueJacketImage from '../assets/images/blue_jacket_and_white_stripe_tee.jpg';
import ModernBlackLeatherSuitImage from '../assets/images/blue_leather_jacket.jpg';
import SpringPrintedDressImage from '../assets/images/spring_printed_dress.jpg';
import ModernLoveTeeImage from '../assets/images/modern_love_tee.jpg';
import BlackJacketImage from '../assets/images/black_leather_jacket.jpg';
import HipsterBlackTopImage from '../assets/images/hipster_black_top.jpg';
import CasualLeatherBeltsImage from '../assets/images/casual_leather_belts.jpg';
import LeatherGlovesImage from '../assets/images/leather_gloves.jpg';
import ModernLeatherBootsImage from '../assets/images/modern_leather_boots.jpg';
import BrownDressShoesImage from '../assets/images/brown_dress_shoes.jpg';

export default {
  data() {
    return { //array varie categorie per card
      categories: [ 
        {
          name: "Men", //MEN
          cards: [
            {
              id: 1,
              image: ElegantImage,
              title: "Black Leather Jacket",
              subtitle: "Men, Jackets, Jeans",
              originalPrice: "$235",
              price: "$200",
              discountPrice: true,

            },
            {
              id: 2,
              image: BlackLeatherSuitImage,
              title: "Black Leather Suit",
              subtitle: "Jackets, Men",
              price: "$176",
            },
            {
              id: 3,
              image: BlueJacketImage,
              title: "Blue Jacket & Stripe Tee",
              subtitle: "Jackets, Men, Suits",
              price: "$580",
            },
            {
              id: 4,
              image: ModernBlackLeatherSuitImage,
              title: "Modern Black Leather Suit",
              subtitle: "Jackets, Men",
              price: "$96",
            },
          ],
        },
        {
          name: "Women", //women
          cards: [
            {
              id: 5,
              image: SpringPrintedDressImage,
              title: "Spring Printed Dress",
              subtitle: "Dress, Women",
              price: "$47",
            },
            {
              id: 6,
              image: ModernLoveTeeImage,
              title: "Modern Love Tee",
              subtitle: "T-Shirts, Women",
              price: "$68",
            },
            {
              id: 7,
              image: BlackJacketImage,
              title: "Black Jacket",
              subtitle: "Jackets, Women",
              price: "$125",
            },
            {
              id: 8,
              image: HipsterBlackTopImage,
              title: "Hipster Black Top",
              subtitle: "T-Shirts, Women",
              price: "$57",
            },
          ],
        },
        {
          name: "Accessories", //Accessories
          cards: [
            {
              id: 9,
              image: CasualLeatherBeltsImage,
              title: "Casual Leather Belts",
              subtitle: "Accessories, Men",
              price: "$65",
            },
            {
              id: 10,
              image: LeatherGlovesImage,
              title: "Leather Gloves",
              subtitle: "Accessories, Gloves, Men, Women",
              price: "$45",
            },
            {
              id: 11,
              image: ModernLeatherBootsImage,
              title: "Modern Leather Boots",
              subtitle: "Accessories, Men, Miscellaneous, Shoes",
              originalPrice: "$50",
              price: "$30",
              discountPrice: true,
            },
            {
              id: 12,
              image: BrownDressShoesImage,
              title: "Brown Dress Shoes",
              subtitle: "Accessories, Miscellaneous, Shoes, Women",
              originalPrice: "$46",
              price: "$36",
              discountPrice: true,
            },
          ],
        },
      ],
      activeCategory: { //card visibili di default
        name: "Men",
        cards: [
          {
            id: 1,
            image: ElegantImage,
            title: "Black Leather Jacket",
            subtitle: "Men, Jackets, Jeans",
            originalPrice: "$235",
            price: "$200",
            discountPrice: true,
          },
          {
            id: 2,
            image: BlackLeatherSuitImage,
            title: "Black Leather Suit",
            subtitle: "Jackets, Men",
            price: "$176",
          },
          {
            id: 3,
            image: BlueJacketImage,
            title: "Blue Jacket & Stripe Tee",
            subtitle: "Jackets, Men, Suits",
            price: "$176",

          },
          {
            id: 4,
            image: ModernBlackLeatherSuitImage,
            title: "Modern Black Leather Suit",
            subtitle: "Jackets, Men",
            price: "$176",

          },
        ],
      },
      cardOptions: {},
    };
  },
  methods: {
    changeCategory(category) {
      this.activeCategory = category;
    },
    showCardOptions(cardId) {
      this.cardOptions[cardId] = true;
    },
    addToCart(cardId) {
      console.log(`Added product with ID ${cardId} to cart.`);
    },
    showDetails(cardId) {
      console.log(`Show details for product with ID ${cardId}.`);
    },
  },
};
</script>

  
<style scoped>
.shop-container {
  margin-top: 20px;
  margin-bottom: 50px;
  text-align: center;
}

.menu {
  display: flex;
  margin-bottom: 2rem;
  justify-content: center;
  font-size: 1.5rem;
  padding: 2px;
}

.menu button {
  border: solid 1px gray;
  color: gray;
}

.cards {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  justify-content: center;
}

.card {
  position: relative;
  overflow: hidden;
  text-align: center;
  max-width: 20%;
  max-height: 20%;
  border: none;
}


.card p {
    margin: 0;
}

.original-price {
    text-decoration: line-through;
    margin-right: 0.5rem; 
}
.card img {
  width: 100%;
  height: auto;
  transition: transform 0.3s ease-in-out;
}



.card .info {
  padding: 1rem;
  transform: translateY(0);
}

.card:hover img {
  background: linear-gradient(180.3deg, rgb(214, 224, 255) 37.2%, rgb(254, 168, 168) 137.3%);
}
.card-options {
  display: none;
  position: absolute;
  top: 40%;
  left: 50%;
  width: 302px;
  height: 400px;
  transform: translate(-50%, -50%);
  background: linear-gradient(180.3deg, rgb(214, 224, 255) 37.2%, rgb(254, 168, 168) 137.3%);
  padding: 1rem;
  text-align: center;
}

.card:hover .card-options {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.card-options a {
  text-decoration: none;
  padding: 0.5rem 1rem;
  display: block;
}

.card-options i {
  margin-bottom: 0.5rem;
  font-size:small;
  color: white;
}
</style>
