<template>
    <div>
        <Header/>
        <div class="bd_l" :style="bgImage">
            <div class="content-section">
                <div class="row sr">
                    <div class="col-md-6 float-left">
                        <p class="pt-2">Recipes Available - ({{ returnCount }})</p>
                    </div>

                    <div class="col-md-6">
                        <form class="form-inline float-right" method="GET">
                            <label class="sr-only" for="inlineFormInputName2">Name</label>
                            <input type="text" class="form-control mb-2 mr-sm-2" id="inlineFormInputName2" placeholder="Search Recipe......">
                            <button type="submit" class="btn btn-outline-success mb-2">Submit</button>
                        </form>
                    </div>
                </div>

                <div class="row">
                    <div class="col-md-4 d-flex justify-content-center" v-for="ln in lunch" :key="ln.id">
                        <div class="bf glass">
                            <div class="media">
                                <div class="media-body">
                                    <img class="rounded-circle account-img" :src="ln.image" alt="">
                                    <h5 class="card-title" style="color: #fff; font-weight: bold; padding-bottom: 10px;">{{ ln.name }}</h5>
                                    <router-link :to="{name: 'Details', params: {id: ln.id}}" class="bn">View Full Recipe</router-link>
                                </div>
                            </div>
                        </div>
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
    name: 'Lunch',
    components:{
        Header,
        Footer
    },
    data(){
        return{
            bgImage:{
                backgroundImage: `linear-gradient(rgba(0,0,0,0.8),rgba(0,0,0,0.8)), url(${require('@/assets/images/bf.jpg')})`
            },
            Recipe: []
        }
    },
    methods:{
        getLunch(){
            axios.get('http://127.0.0.1:8000/Recipe/')
            .then(res => (this.Recipe = res.data))
            .catch(err => console.log(err))
        }
    },
    computed:{
        lunch() {
            return this.Recipe.filter(x => x.category == 'Lunch')
        },
        returnCount(){
            return this.Recipe.filter(x => x.category == 'Lunch').length
        }
    },
    mounted(){
        this.getLunch()
    }
}
</script>
