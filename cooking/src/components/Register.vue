<template>
    <div>
        <Header/>
        <div class="register">
            <div class="row reg_rw justify-content-center">
                <div class="col-md-6 reg_img" :style="bgImage">
                    
                </div>
                <div class="col-md-6 reg_frm">
                    <h2 class="pt-3">Create Account</h2>
                    <div class="condition pt-2 pb-3">
                        <span>By Signing up you agree to the <a href="#">Terms and conditions</a></span>
                    </div>
                    <form>
                        <div class="form-group">
                            <label for="">Username</label>
                            <input type="text" class="form-control" id="" autocomplete="off" placeholder="Jane Doe">
                          </div>
                        <div class="form-group">
                          <label for="">Email</label>
                          <input type="email" class="form-control" id="" autocomplete="off" placeholder="someone@gmail.com">
                        </div>
                        <div class="form-group">
                          <label for="">Password</label>
                          <input type="password" class="form-control" id="" autocomplete="off" placeholder="**********">
                        </div>
                        <div class="form-group">
                            <label for="">Password Confirmation</label>
                            <input type="password" class="form-control" id="" autocomplete="off" placeholder="**********">
                          </div>
                        <button type="submit" class="btn btn-block btn-success">Enter</button>
                    </form>

                    <div class="terms text-center mt-2">
                        <span>Already have an Account?? <router-link to="/login">Login Here</router-link></span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'

export default {
    name: 'Register',
    data(){
        return{
            bgImage:{
                backgroundImage: `linear-gradient(rgba(0,0,0,0.3),rgba(0,0,0,0.3)), url(${require('@/assets/images/food1.jpg')})`
            }
        }
    },
    components:{
        Header,
    }
}
</script>

<style scoped>
.registration .profile{
    color: #fff;
}

.reg_img{
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 94vh;
}

.reg_rw{
    margin-right: 0 !important;
}

.reg_frm{
    padding: 80px 150px;
}

.reg_frm h2{
    font-weight: bold;
    position: relative;
}

.reg_frm h2::after{
    display: block;
    content: '';
    width: 90%;
    height: 5px;
    background: orange;
    position: absolute;
    bottom: -10px;
    left: 0;
}

.register a{
    color: orangered;
    text-decoration: underline;
}

.register .terms span{
    display: block;
}

@media only screen and (max-width: 768px) and (min-width: 426px) {
    .reg_frm {
        padding: 40px 30px;
    }
}

@media only screen and (max-width: 425px) {
    .reg_img {
        height: 0vh;
    }

    .reg_frm {
        padding: 20px 50px;
    }
}
</style>