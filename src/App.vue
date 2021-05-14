<template>

  <div id="app" class="containers">
    <nav class="navbar navbar-expand-sm bg-light">
      <ul class="navbar-nav">
        <div class="logoo"><img src="@/assets/thrifty.png" height="70px"/></div>
        <li class="nav-item">
          <router-link :to="{ name: 'Homepage' }" class="nav-link">HomePage</router-link>
        </li>
        <li class="nav-item">
          <router-link :to="{ name: 'Create' }" class="nav-link">Shop</router-link>
        </li>
        <li class="nav-item">
          <router-link :to="{ name: 'Index' }" class="nav-link">All Items</router-link>
        </li>
        <li class="nav-item">
          <router-link :to="{ name: 'Contacts' }" class="nav-link">Contacts</router-link>
        </li>
      </ul>
    </nav>
    <transition name="fade">
      <div class="gap">
        <router-view></router-view>        
      </div>
    </transition>
  </div>
</template>

<script>

export default {
}
</script>

<style>
    .fade-enter-active, .fade-leave-active {
      transition: opacity .5s
    }
    .fade-enter, .fade-leave-active {
      opacity: 0
    }
    .gap {
      margin-top: 50px;
    }
    .title {
      text-align: center;
      font-size: 50px;
      font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    }
    .intro {
      text-align: center;
    }
    .first {
      height: 400px;
    }
    .card {
      margin-top: 800px;
      width: 500px;
      margin-left: 400px;
      margin-bottom: 100px;
    }
  .card1 {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  max-width: 300px;
  margin: 10px;
  text-align: center;
  font-family: arial;
  float: left;
  margin-left: 50px;

}

.price {
  color: grey;
  font-size: 22px;
}

.containers{
  overflow: hidden;
}

.containers li {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 15px;
  float: right;
}

.containers li:hover {
  background-color: #ddd;
  color: black;
}

.containers li.active {
  background-color: #04AA6D;
  color: white;
  
}
.logo img {
  position: absolute;
  margin-top: 15px;
  margin-left: 10px;
}
h1 {
  font-size: 50px;
  text-align: center;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}
.intro {
  position: relative;
  max-width: 800px;
  margin: 0 auto; 
}
.intros .contents {
  position: absolute; 
  bottom: 0; 
  background: rgb(0, 0, 0); 
  background: rgba(0, 0, 0, 0.5); 
  color: #f1f1f1; 
  width: 100%; 
  padding: 20px; 
  padding-bottom: 50px;
}
.intros img {vertical-align: middle;}

.back {
  display: flex;
  align-items: center;
  padding-bottom: 50px;
}
.img {
  max-width: 100%;
}
.back > div{
  flex-basis: 50%;
}
h4 {
  font-family: Arial, Helvetica, sans-serif;
  letter-spacing: 3px;
}
.footer {
   position: fixed;
   left: 0;
   bottom: 0;
   width: 100%;
   background-color: black;
   color: white;
   text-align: center;
   padding-bottom: 20px;
   padding-top: 20px;
   font-family: Arial, Helvetica, sans-serif;
}
h5 {
  text-align: center;
  font-family: Verdana, Geneva, Tahoma, sans-serif
}

</style>