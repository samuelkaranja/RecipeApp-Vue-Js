<template>
  <div id="app">
    <div id="nav">
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

*{
    margin: 0;
    padding: 0;
    font-size: 16px;
}

.content-section{
    width: 1200px;
    height: 90vh;
    margin: 0 auto;
}

.glass{
    width: 80%;
    height: 32vh;
    padding: 20px 0;
    text-align: center;
    box-shadow: 0 0 1rem 0 rgba(0, 0, 0, .2); 
    border-radius: 5px;
    background-color: rgba(255, 255, 255, .15);
    backdrop-filter: blur(5px);
}

.bd_1{
    background-repeat: no-repeat; 
    background-position: center center; 
    background-size: cover; 
    // padding-bottom: 240px; 
    // padding-top: 20px;
}

.bd_l .sr{
    padding-top: 15px;
    padding-bottom: 30px;
}

.bd_l .sr p{
    color: #fff;
}

.bd_l .bf{
    margin-bottom: 20px;
    text-align: center;
    height: 270px;
}

.bd_l .bf .account-img{
    width: 130px;
    height: 130px;
    object-fit: cover;
    margin-bottom: 5px;
}

.bd_l .media-body .bn{
    border: 1px solid #c74e61;
    border-radius: 50px;
    padding: 10px 20px;
    color: #fff;
    text-decoration: none;
    font-weight: 400;
}

.bd_l .media-body .bn:hover{
    background-color: #c74e61;
    color: #fff;
    border: none;
}
</style>
