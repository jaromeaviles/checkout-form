<template>
    <div class="col-lg-6">
        <div class="card-container">
            <h1>Payment Information</h1>

            <div class="card-information">
                <div class="card-image-container">
                    <img :src="require('@/assets/card.jpeg')" alt="card" />
                    <div class="overlay">
                        <div class="text-overlay-header">
                            <img :src="require('@/assets/chip.png')" alt="chip" />
                            <div class="overlay-name">
                                <p>&#x23; &#x23; &#x23; &#x23;</p>
                                <p>&#x23; &#x23; &#x23; &#x23;</p>
                                <p>&#x23; &#x23; &#x23; &#x23;</p>
                                <p>&#x23; &#x23; &#x23; &#x23;</p>
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
    data() {
        return {
            
        }
    }
}
</script>

<style lang="scss" scoped>
    h1 {
        font-size: 18px;
        margin-bottom: 10px;
        text-align: left;
    }
    .card-information {
        background-color: white;
        padding: 30px;
        border-radius: 5px;
        .card-image-container {
            position: relative;
            width: 340px;
            margin: 0 auto;
            >img {
                object-fit: cover;
                width: 100%;
                border-radius: 15px;
                box-shadow: rgba(17, 17, 26, 0.1) 0px 8px 24px, rgba(17, 17, 26, 0.1) 0px 16px 56px, rgba(17, 17, 26, 0.1) 0px 24px 80px;
            }
            .overlay {
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background-color: rgba(0, 0, 0, 0.5);
                padding: 15px;
                border-radius: 15px;
                img {
                    width: 50px;
                    height: 40px;
                }
                .text-overlay-header {
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;
                    height: 100%;
                    color: white;

                    .overlay-name {
                        display: flex;
                        flex-direction: row;
                        justify-content: space-between;
                        width: 270px;

                        p {
                            font-size: 18px;
                        }
                    }
                }
            }
        }
    }
</style>