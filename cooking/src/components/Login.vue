<template>
    <div>
        <Header/>
        <div class="login">
            <div class="row reg_rw justify-content-center">
                <div class="col-md-6 lg_frm">
                    <h2 class="pt-3 pb-4">Login</h2>
                    <form>
                        <div class="form-group">
                          <label for="">Username</label>
                          <input type="text" class="form-control" id="" placeholder="Jane Doe">
                        </div>
                        <div class="form-group">
                          <label for="">Password</label>
                          <input type="password" class="form-control" id="" placeholder="**********">
                        </div>
                        <button type="submit" class="btn btn-block btn-success">Enter</button>
                    </form>
                    <div class="rg text-center mt-2">
                        <div class="float-right">
                            <span><a href="">Forgot Password??</a></span>
                        </div>

                        <div class="float-left">
                            <span>New Here?? <router-link to="/register">Register Here</router-link></span>
                        </div>
                    </div>
                </div>

                <div class="col-md-6 lg_img" :style="bgImage"></div>
            </div>
        </div>
    </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'

export default {
    name: 'Login',
    data(){
        return{
            bgImage:{
                backgroundImage: `linear-gradient(rgba(0,0,0,0.3),rgba(0,0,0,0.3)), url(${require('@/assets/images/food2.jpg')})`
            }
        }
    },
    components:{
        Header,
    }
}
</script>

<style scoped>
.reg_rw{
    margin-right: 0 !important;
}

.lg_img{
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 94vh;
}

.lg_frm{
    padding: 130px 180px;
}

.lg_frm h2{
    font-weight: bold;
    position: relative;
}

.lg_frm h2::after{
    display: block;
    content: '';
    width: 90%;
    height: 5px;
    background: orange;
    position: absolute;
    bottom: 15px;
    left: 0;
}

.lg_frm .rg a{
    color: orangered;
    text-decoration: underline;
}

@media only screen and (max-width: 768px) and (min-width: 426px) {
    .lg_frm {
        padding: 30px 50px;
    }

    .lg_img {
        height: 60vh;
    }

    .reg_rw {
        margin-top: 80px;
    }

    .reg_frm {
        padding: 20px 30px;
    }
}

@media only screen and (max-width: 425px) {
    .lg_img {
        height: 0vh;
    }

    .lg_frm {
        padding: 50px;
    }
}
</style>