<template>
    <footer>
        <div class="ms_container pt-3">
            <div class="row">
                <div class="col-6">
                    <div class="row footer-left">
                        <div class="col-8">
                            <img :src="require('../assets/theme_eduprime_logo.png')" alt="">
                            <p>EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc</p>
                            <div class="social-icon-wrapper">
                                <a href=""><i class="fab fa-facebook-f"></i> </a>
                                <a href=""> <i class="fab fa-twitter"></i></a>
                                <a href=""><i class="fab fa-instagram"></i></a>
                                
                            </div>
                        </div>
                        <div class="col-4">
                            <h5>Get EduPrime</h5>
                            <ul>
                                <li><a href="">Request a website</a></li>
                                <li><a href="">Browse Themes</a></li>
                                <li><a href="">Payment options</a></li>
                                <li><a href="">Support System</a></li>
                                <li><a href="">Checkout</a></li>
                                <li><a href="">Purchase Theme</a></li>

                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col-6">
                    <div class="row footer-right">
                        <div class="col-4">
                            <h5>Networking</h5>
                            <ul>
                                <li><a href="">Purchase Theme</a></li>
                                <li><a href="">Our Benefits</a></li>
                                <li><a href="">Our Teams</a></li>
                                <li><a href="">Our Services</a></li>
                                <li><a href="">Other Product</a></li>
                                <li><a href="">My account</a></li>

                            </ul>
                        </div>
                        <div class="col-8">
                            <input type="text" placeholder="Search...">
                            <button class="btn rounded-pill ms-n5" type="button">
                                <i class="fa fa-search"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
            </div>
        </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style>
footer {
    background-color: #e56768;
    color: white;
    padding: 3rem 0;
}

.footer-left p {
    padding: 1.5rem 0;
}

.footer-left img {
    width: 10rem;
}

.social-icon-wrapper i {
    font-size: 1.2rem;
    border: 1px solid #e9d758;
    border-radius: 50%;
    margin: 0 .5rem;
    text-align: center;
    line-height: 1.2rem;
    padding: .5rem;
}

h5 {
    font-size: .9rem!important;
}

ul {
    margin: 0!important;
    padding: 0!important;
}

li {
    font-size: .7rem;
}

.footer-right input {
    width: 10rem;
    border: 0;
    border-radius: 20px;
    margin-left: 3rem;
    padding: .6rem 1.5rem;
    font-size: .8rem;
}

button {
    background-color: #e9d758;
}

.ms-n5 {
    margin-left: -40px;
}


</style>