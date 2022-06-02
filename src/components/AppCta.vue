<template>
    <section>
        <div class="newsletter">
            <div class="ms_container">
                <h4>Subscribe Now to Our Newsletter</h4>
                <input type="text" placeholder="Email address...">
            </div>
        </div>

        <div class="partner">
            <div class="ms_container pt-3">
                <h3>Partners</h3>
                <p>Levarage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy</p>
                <div class="img-wrapper d-flex justify-content-center align-items-center p-3">
                    <div class="partner-img" v-for="(item, index) in partnerImg" :key="index">
                        <img :src="require(`../assets/${item.img}`)" alt="">
                    </div>
                </div>
            </div>
        </div>



    </section>
</template>

<script>
export default {
    data() {
        return {
            partnerImg: [
                {
                    img: "partner-2.png"
                },
                {
                    img: "partner-3.png"
                },
                {
                    img: "partner-4.png"
                },
                {
                    img: "partner-5.png"
                },
                {
                    img: "partner-6.png"
                },
                {
                    img: "partner-8.png"
                },
                {
                    img: "partner-1.png"
                },
                {
                    img: "partner-7.png"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

.newsletter {
    padding: 3rem;
    background-color: #e56768;

    h4 {
        color: white;
        display: inline-block;
    }
}

.partner {
    text-align: center;

    .partner-img {
        color: lightgray;
        padding-bottom: 4rem;

        > img {
            padding: 0 1rem;
            filter: invert(50%);
        }
    }

    .partner-img >img:hover {
        filter: invert(0%);
    }
}
</style>