<template>
    <div class="container-fluid text-white py-4 MyColor">
        <div class="row">
            <!-- Lista 1 -->
            <div class="col-md-3">
                <img src="../assets/images/classic_shop_logo_footer.png" alt="Logo" class=" mb-3 w-50 MyMargin">
                <ul class="list-unstyled MyMargin">
                    <li>12345 North Main Street,</li>
                    <li>New York, NY 555555</li>
                    <li>Phone: 1.800.555.6789</li>
                    <li>Email: info@company.com</li>
                    <li>Web: Theme-fusion.com</li>
                </ul>
                <div class="d-flex MyMargin">
                    <i class="fab fa-facebook-square me-2"></i>
                    <i class="fab fa-twitter-square me-2"></i>
                    <i class="fab fa-instagram-square me-2"></i>
                    <i class="fab fa-pinterest-square"></i>
                </div>
            </div>

            <!-- Lista 2 -->
            <div class="col-md-3">
                <h5>TOP RATED PRODUCTS</h5>
                <div v-for="card in cardArray" :key="card.id" class="card MyCard mb-3">
                    <div class="row g-0">
                        <div class="col-md-4">
                            <img :src="card.image" class="img-fluid rounded-start MyImg" alt="Card Image">
                        </div>
                        <div class="col-md-8">
                            <div class="card-body">
                                <h5 class="card-title">{{ card.title }}</h5>
                                <div class="rating">
                                    <span v-for="star in card.stars" :key="star" class="star">&#9733;</span>
                                </div>
                                <p class="card-text">{{ card.price }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Lista 3 -->
            <div class="col-md-3">
                <div class="component-container">
                    <div class="card-container">
                        <h5>RECENT POSTS</h5>
                        <div v-for="card in selectedCards" :key="card.id" class="card MyCard">
                            <img :src="card.image" alt="Card Image">
                            <div class="card-info">
                                <h5>{{ card.title }}</h5>
                                <h6>{{ card.subtitle }}</h6>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Lista 4 -->
            <div class="col-md-3">
                <h5>TAGS</h5>
                <div class="row">

                    <div class="list">
                       
                        <div class="tags">
                            <div class="row">
                               
                                <div class="col-6">
                                    <div class="mb-2">
                                        <button type="button" class="btn MyBtn tag-button">Winter</button>
                                    </div>
                                    <div class="mb-2">
                                        <button type="button" class="btn MyBtn tag-button">Winter</button>
                                    </div>
                                    <div class="mb-2">
                                        <button type="button" class="btn MyBtn tag-button">Winter</button>
                                    </div>
                                    <div class="mb-2">
                                        <button type="button" class="btn MyBtn tag-button">Winter</button>
                                    </div>
                                    
                                    
                                </div>

                              
                                <div class="col-6">
                                    <div class="mb-2">
                                        <button type="button" class="btn MyBtn tag-button">Winter</button>
                                    </div>
                                    <div class="mb-2">
                                        <button type="button" class="btn MyBtn tag-button">Winter</button>
                                    </div>
                                    <div class="mb-2">
                                        <button type="button" class="btn MyBtn tag-button">Winter</button>
                                    </div>
                                    <div class="mb-2">
                                        <button type="button" class="btn MyBtn tag-button">Winter</button>
                                    </div>
                                    
                                </div>
                            </div>
                        </div>
                      
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>
import card1 from '../assets/images/spring_printed_dress-120x156.jpg';
import card2 from '../assets/images/leather_gloves-120x156.jpg';
import card3 from '../assets/images/black_elegant_leather_jacket-120x156.jpg';
import card4 from '../assets/images/blue_leather_jacket-120x156.jpg';
import Post1 from '../assets/images/post_img_10-320x202.jpg';
import Post3 from '../assets/images/post_img_12-320x202.jpg';

export default {
    data() {
        return {
            cardArray: [
                {
                    id: 1,
                    image: card1,
                    title: 'Spring Printed Dress',
                    stars: 5,
                    price: '$47',

                },
                {
                    id: 2,
                    image: card2,
                    title: 'Leather Gloves',
                    stars: 5,
                    price: '$45',

                },
                {
                    id: 31,
                    image: card3,
                    title: 'Black Leather Jacket',
                    stars: 5,
                    price: '$200',

                },
                {
                    id: 4,
                    image: card4,
                    title: 'Digital Download',
                    stars: 5,
                    price: '$59',

                },
                
            ],
            selectedCards: [
                {
                    id: 1,
                    image: Post1,
                    title: "Aenean lobortis sapien enim viverra",
                    subtitle: "Markup, News, Trends",
                },
                {
                    id: 3,
                    image: Post3,
                    title: "Nunc fermint nulla eu justo sem id",
                    subtitle: "Markup, News, Trends",
                },
            ],


        };
    },
};
</script>
  
<style scoped>

.MyBtn{
    background-color: transparent;
    border: 1px solid white;
    color: white;
}
.tag-button:hover {
    background-color: turquoise;
    
}

.MyCard {
    background-color: transparent;
    border: none;
    border-bottom: 0.2px solid white;
    height: 18%;
    margin-top: 6%;
}

.MyColor {
    background-color: #2B2E32;
}

.MyImg {
    height: 86%;
}

.MyMargin {
    margin-left: 6%;
}
</style>
  