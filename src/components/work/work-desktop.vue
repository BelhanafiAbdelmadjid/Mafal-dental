<template>
    <div class="work-holder" >
        <h1 class="titre-info"  style="color: var(--gray-text-color);" >Notre travail</h1>
        <div class="content content-left">
            <swiper autoplay :delay="1000" :slides-per-view="1" :space-between="10" @swiper="onSwiper" @slideChange="onSlideChange">
                <swiper-slide>
                    <div class="slide">
                      <div class="slider-image"
                      :style="{ backgroundImage: `url(${firstWork})` }"> 
                      </div>
                      <div class="description" >
                        <h2 style="color: var(--gray-text-color);" >Nouveau sourire 😀</h2>
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
                      <div class="slider-image"
                      :style="{ backgroundImage: `url(${secondWork})` }"> 
                      </div>
                      <div class="description" >
                        <h2 style="color: var(--gray-text-color);" >Couronnes en céramique 👌🏻</h2>
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
                      <div class="slider-image"
                      :style="{ backgroundImage: `url(${thirdWork})` }"> 
                      </div>
                      <div class="description" >
                        <h2 style="color: var(--gray-text-color);" >Bridge en céramique ✨</h2>
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

import { Swiper, SwiperSlide,useSwiper } from 'swiper/vue';
import 'swiper/css';
export default{
    data(){
        return{
            firstWork:firstWork,
            secondWork:secondWork,
            thirdWork:thirdWork,

            slideIndex:0,
        }
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
    components : {
        Swiper,
    SwiperSlide,
    },
    setup() {
        const onSwiper = (swiper) => {
        console.log(swiper);
        };
        const swiper = useSwiper();
        // $refs.swiper = swiper;
        
        function next() {
            swiper.value.slideNext() // should work
            }
        return {
            onSwiper,swiper,next
        }
  }
  
}
</script>

<style scoped >
.work-holder{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    gap : 50px;
  }
.content{
    width: 800px;
    height: 40vh;

    border-radius: 10px; 
    overflow: hidden;


    -webkit-box-shadow:0px 10px 39px 10px rgba(62,66,66,0.22);
  -moz-box-shadow: 0px 10px 39px 10px rgba(62,66,66,0.22);
  box-shadow: 0px 10px 39px 10px rgba(62,66,66,0.22);

  position :relative;

}
.content .radios{
    position :absolute;
    width: 100%;
    bottom: 0;
    left:0;
    z-index: 999;

    display: flex;
    justify-content: center;
    align-items: center;

    padding: 10px;
    box-sizing: border-box;

    gap:7px;
}

.slider-image{
  width: 100%;
  height: 40vh;

  background-size: cover; 
  background-position: center center; 
  background-repeat: no-repeat; 
  background-color: #f0f0f0;
}
.content .slide{
  display: flex;
  justify-content: center;
  align-items: center;
}
.content .slide .description{
  width: 100%;
  height: 40vh;

  padding: 10px;
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