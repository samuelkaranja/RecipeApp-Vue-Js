<template>
    <div>
        <Header/>
        <div class="details" :style="bgImage">
            <div class="container">
                <div class="row">
                    <div class="col-md-12">
                        <div class="header">
                            <h1 class="text-center pt-3 pb-4">{{ recipe.name }}</h1>
                        </div>
                    </div>
                </div>

                <div class="row">
                    <div class="col-md-6 image-wrapper">
                        <img :src="recipe.image" class="img-fluid" alt="...">
                    </div>

                    <div class="col-md-6 ng detail_glass">
                        <h3>Ingredients</h3>
                        <div v-html="recipe.ingredients"></div>    
                    </div>
                </div>

                <div class="row">
                    <div class="col-md-9 pr detail_glass">
                        <h3 class="pt-3 pb-2">Procedure</h3>
                        <div v-html="recipe.procedure"></div>
                    </div>
                </div>
            </div>
        </div>
        <Footer/>
    </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import axios from 'axios'


export default {
    name: 'Details',
    computed: {
        id() {
            return this.$route.params.id
        }
    },
    components:{
        Header,
        Footer
    },
    data(){
        return {
            recipeId:this.$route.params.id,
            recipe: {},
            bgImage:{
                backgroundImage: `linear-gradient(rgba(0,0,0,0.7),rgba(0,0,0,0.7)), url(${require('@/assets/images/bf.jpg')})`
            }
        }
    },
    methods: {
        getRecipe() {
            axios.get(`http://localhost:8000/Recipe/${this.id}`)
            .then(resp => (this.Recipe = resp.data))
            .then((data) => {
                console.log(data)
                this.recipe = data
            })
        }
    },
    mounted() {
        this.getRecipe();
    },
}
</script>

<style scoped>

.details{
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    padding: 20px 0;
}

.details .header h1{
    color: #ffffff;
    font-weight: bold;
}

.details .header h1::after{
  content:  '';
  display: block;
  padding-bottom: 8px;
  width: 100%;
  border-bottom: 4px solid orange;
  margin-bottom: 20px;
}

.details .img-fluid{
    height: 50vh !important;
    width: 100%;
    object-fit: cover;
    margin-bottom: 20px;
    border-radius: 10px;
}

.details .image-wrapper{
    overflow: hidden;
}

.details .ng{
    padding-left: 55px;
    color: #ffffff;
}

.details .ng h3{
    padding-bottom: 12px;
    font-weight: bold;
    color: #ffffff;
}

.details .ng h3::after{
  content:  '';
  display: block;
  padding-bottom: 8px;
  width: 60%; 
  border-bottom: 4px solid orange;
}

.details .pr{
    padding: 10px 40px 80px 40px;
    margin-top: 50px;
    color: #ffffff;
    font-weight: 300;
}

.details .pr h3{
    padding-bottom: 12px;
    font-weight: bold;
    color: #ffffff;
}

.details .pr h3::after{
  content:  '';
  display: block;
  padding-bottom: 8px;
  width: 60%; 
  border-bottom: 4px solid orange;
}

.details .ng ol li{
    padding-bottom: 25px;
}

.detail_glass{
    width: 100%;
    padding: 15px 0;
    box-shadow: 0 0 1rem 0 rgba(0, 0, 0, .2); 
    border-radius: 20px;
    background-color: rgba(255, 255, 255, .15);
    backdrop-filter: blur(5px);
}

</style>