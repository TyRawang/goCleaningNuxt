<template>
    <!-- Banner -->
    <div id="banner" >
        <div class="banner-bg">
            <div class="container">
                <!-- <h1>Best Janitorial Service in Calgary</h1>
                <h3>Fully Insured, Bonded & WCB</h3> -->

                <div class="banner-form commercial">
                    <!-- <div class="meter orange nostripes">
                        <span style="width: 33.3%"></span>
                    </div> -->
                    <h1>Carpet Cleaning Service Calgary</h1>
                    <h5>Schedule Your Carpet Cleaning <span>At Your Demand</span></h5>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
name: "TheCarpetBanner"
}
</script>

<style scoped>
    #banner {
        width: 100%;
        height: auto;
        background: url('~assets/img/Go-Cleaning-Office-Cleaning.jpg') no-repeat center center/cover;
        /* border-radius: 0% 0% 90% 90%/0% 0% 50% 50%; */
    }

    #banner .banner-bg {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        padding-top: 4rem;
        /* background-color: rgba(73, 243, 51, 0.7); */
        background-color: rgba(153, 115, 226, 0.8);
        width: 100%;
        height: auto;
        /* border-radius: 0% 0% 90% 90%/0% 0% 50% 50%; */

    }

    #banner .banner-form.commercial h1 {
        color: #ffffff;
    } 

    #banner .banner-form {
        /* background: rgb(255, 255, 255, 0.5); */
        border-radius: 15px;
        padding: 30px 10px 90px 10px;
        width: 100%;
        height: auto;
    }


    


</style>