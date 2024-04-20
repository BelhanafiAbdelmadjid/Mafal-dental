<template>
    <div class="work-holder" >
        <h1 style="color: var(--gray-text-color);" >Notre travail</h1>
        <div class="content">
            <swiper :slides-per-view="1" :space-between="50" @swiper="onSwiper" @slideChange="onSlideChange">
                <swiper-slide>
                    <div class="slide">
                        <h2 style="color: var(--gray-text-color);" >Nouveau sourire 😀</h2>
                      <div class="slider-image"
                      :style="{ backgroundImage: `url(${firstWork})` }"> 
                      </div>
                      <div class="description" >
                        
                        <p>
                          Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                          Eos eligendi, culpa dicta sit eum a doloribus provident dolore magnam ab aperiam ipsa,
                          voluptatum molestiae excepturi doloremque illum dolorum libero consequatur?
                        </p>
                      </div>
                      
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="slide">
                        <h2 style="color: var(--gray-text-color);" >Couronnes en céramique 👌🏻</h2>
                      <div class="slider-image"
                      :style="{ backgroundImage: `url(${secondWork})` }"> 
                      </div>
                      <div class="description" >
                        <p>
                          Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                          Eos eligendi, culpa dicta sit eum a doloribus provident dolore magnam ab aperiam ipsa,
                          voluptatum molestiae excepturi doloremque illum dolorum libero consequatur?
                        </p>
                      </div>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="slide">
                        <h2 style="color: var(--gray-text-color);" >Bridge en céramique ✨</h2>

                      <div class="slider-image"
                      :style="{ backgroundImage: `url(${thirdWork})` }"> 
                      </div>
                      <div class="description" >
                        <p>
                          Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                          Eos eligendi, culpa dicta sit eum a doloribus provident dolore magnam ab aperiam ipsa,
                          voluptatum molestiae excepturi doloremque illum dolorum libero consequatur?
                        </p>
                      </div>
                    </div>
                </swiper-slide>
            </swiper>
            <div style="pointer-events: none" class="radios">
                <input @click="SlideTo(0)"  :checked="slideIndex==0" type="radio" name="slide" >
                <input @click="SlideTo(1)"  :checked="slideIndex==1" type="radio" name="slide">
                <input @click="SlideTo(2)"  :checked="slideIndex==2" type="radio" name="slide">
            </div>
        </div>
    </div>
</template>
<script>
import firstWork from "../../assets/images/first_work.jpg"
import secondWork from "../../assets/images/second_work.jpg"
import thirdWork from "../../assets/images/third_work.jpg"

import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
export default{
    data(){
        return{
            firstWork:firstWork,
            secondWork:secondWork,
            thirdWork:thirdWork,

            slideIndex:0
        }
    },
    components : {
        Swiper,
    SwiperSlide,
    },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
   
    return {
      onSwiper,
    };
  },
    methods : {
    onSlideChange(swiper){
        this.slideIndex = swiper.realIndex
        },
    SlideTo() {
        console.log("click",this.$refs.swiper)
        // this.$refs.swiper.swiper.slideNext()
    }
    },
}
</script>
<style scoped >
.content .radios{
    position :absolute;
    width: 100%;
    bottom: 0;
    left:0;
    z-index: 99;

    display: flex;
    justify-content: center;
    align-items: center;

    padding: 10px;
    box-sizing: border-box;

    gap:7px;
}
.work-holder{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    min-height: 300px;

    gap : 40px;
  }
.content{
    width: 350px;
    height: auto;
    min-height: 220px;
    border-radius: 10px; 
    overflow: hidden;


    -webkit-box-shadow:0px 10px 39px 10px rgba(62,66,66,0.22);
    -moz-box-shadow: 0px 10px 39px 10px rgba(62,66,66,0.22);
    box-shadow: 0px 10px 39px 10px rgba(62,66,66,0.22);

    position :relative;
}

.slider-image{
  width: 100%;
  height: 40vh;
  min-height: 220px;

  background-size: cover; 
  background-position: center center; 
  background-repeat: no-repeat; 
  background-color: #f0f0f0;
}
.content .slide{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  min-height: 220px;
}
.content .slide h2{
    padding: 5px;
    box-sizing: border-box;
}
.content .slide .description{
  width: 100%;
  height: auto;
  min-height: 220px;

  padding: 10px;
  padding-bottom: 25px;
  box-sizing: border-box;

  display:  flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;


}
.content .slide .description p{
  display: flex;
  justify-content: center;
  align-items: center;

  text-align: center;
  
  height: 100%;
}
@media only screen and (max-width: 1000px) {
  
}
</style>