<template>
  <!--sezione post per il blog-->
    <div class="component-container">
      <div class="header">
        <h2>{{ title }}</h2>
        <h4>{{ subtitle }}</h4>
      </div>
      <div class="card-container">
        <div v-for="card in cards" :key="card.id" class="card">
          <img :src="card.image" alt="Card Image" @mouseover="hoverEffect(card.id)">
          <div class="card-info">
            <h5>{{ card.title }}</h5>
            <h6>{{ card.subtitle }}</h6>
            <p>{{ card.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import Post1 from '../assets/images/post_img_10-320x202.jpg';
  import Post2 from '../assets/images/post_img_11-320x202.jpg';
  import Post3 from '../assets/images/post_img_12-320x202.jpg';

export default {
  data() {
    return {
      title: "From Our Blog",
      subtitle: "The latest Classic Shop news",
      cards: [
        {
          id: 1,
          image: Post1,  
          title: "Aenean lobortis sapien enim viverra",
          subtitle: "September 9th, 2015|0 Comments",
          description: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
        },
        {
          id: 2,
          image: Post2,  
          title: "Duis ac massa semper maximus",
          subtitle: "September 9th, 2015|0 Comments",
          description: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
        },
        {
          id: 3,
          image: Post3,  
          title: "Nunc fermint nulla eu justo sem id",
          subtitle: "September 9th, 2015|0 Comments",
          description: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
        },
      ],
      hoveredCard: null,
    };
  },
  methods: {
    hoverEffect(cardId) {
      this.hoveredCard = cardId;
    },
  },
};

  </script>
  
  <style scoped>
  .component-container {
    margin: 20px;
    margin-top: 10%;
  }
  
  .header {
    text-align: center;
    margin-bottom: 20px;
  }
  
  .card-container {
    display: flex;
    justify-content: space-between;
  }
  
  .card {
    width: 30%;
    position: relative;
    overflow: hidden;
    margin-bottom: 20px;
    transition: transform 0.3s ease-in-out;
    border: none;
  }
  
  .card img {
    width: 100%;
    height: auto;
  }
  
  .card img:hover {
    transform: scale(1.1);
  }
  
  .card-info {
    padding: 10px;
    width: 100%;
    background-color: white;
    color: #040404;
    text-align: left;
  }
  
  .card-info h5,
  .card-info h6 {
    margin: 0;
  }
  
  .card-info p {
    margin: 10px 0 0;
  }
  </style>
  