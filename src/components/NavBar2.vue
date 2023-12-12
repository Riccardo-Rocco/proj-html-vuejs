<template>
    <nav class="navbar navbar-expand-lg bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <img src="../assets/images/classic_shop_logo1x.png" alt="Bootstrap" width="150" height="80">
    </a>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav Menu">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Shop</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Products</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Categories</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">News</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Elements</a>
        </li>
        <li class="nav-item">
            <button type="button" class="btn btn-primary rounded-pill">SHOP NOW!</button>
        </li>
      </ul>

      <ul  class="navbar-nav icons">
        <li  class="nav-item icon">
            <a class="nav-link" href=""><i class="fa-regular fa-user"></i></a>
        </li>
        <li  class="nav-item icon">
            <a class="nav-link" href=""><i class="fas fa-bag-shopping"></i></a>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css'; 
</script>

<style scoped>
.container-fluid {
    padding-left: 10%;
}

.Menu{
  padding-left: 10%;  
}
.icons{
   padding-left: 20%;

}

.icons a{
    font-size: x-large;
    
}
.nav-item{
    margin-right: 1rem;
}
</style>