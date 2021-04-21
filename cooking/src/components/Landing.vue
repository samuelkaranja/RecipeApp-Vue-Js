<template>
    <div class="landing" :style="bgImage">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <div class="header text-center">
                        <h1>FIND THE BEST RECIPE'S HERE FOR FREE!!</h1>
                        <h5>Click the links below to explore the different Recipe's Available to you</h5>
                    </div>
                </div>
            </div>

            <div class="row"> 
                <div class="col-md-4">
                    <div class="ld">
                        <div class="media">
                            <div class="media-body">
                                <img class="rounded-circle account-img" src="../assets/images/breakfast.jpg" alt="">
                                <h3><router-link to="/breakfast-recipe" class="nv-link">BreakFast Recipe</router-link></h3>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-md-4">
                    <div class="ld">
                        <div class="media">
                            <div class="media-body">
                                <img class="rounded-circle account-img" src="../assets/images/lunch.jpg" alt="">
                                <h3><router-link to="/lunch-recipe" class="nv-link">Lunch Recipe</router-link></h3>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-md-4">
                    <div class="ld">
                        <div class="media">
                            <div class="media-body">
                                <img class="rounded-circle account-img" src="../assets/images/dinner.jpg" alt="">
                                <h3><router-link to="/dinner-recipe" class="nv-link">Dinner Recipe</router-link></h3>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Landing',
    data(){
        return {
            bgImage:{
                backgroundImage: `linear-gradient(rgba(0,0,0,0.8),rgba(0,0,0,0.8)), url(${require('@/assets/images/food3.jpg')})`
            }
        }
    }
}
</script>

<style scoped>
.landing{
    position: relative;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 92vh;
}

.landing .header{
    color: #fff;
    margin-top: 60px;
}

.ld{
    width: 90%;
    height: 30vh;
    margin-top: 80px;
    padding: 25px 0;
    text-align: center;
    box-shadow: 0 0 1rem 0 rgba(0, 0, 0, .2); 
    border-radius: 5px;
    background-color: rgba(255, 255, 255, .15);
    backdrop-filter: blur(5px);
}

.ld .account-img{
	height: 130px; 
	width: 130px; 
	object-fit: cover;
    margin-bottom: 10px;
}

.ld a{
    color: #fff;
    font-size: 25px;
}
</style>