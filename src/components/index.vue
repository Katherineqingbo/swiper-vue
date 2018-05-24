<template>
  <div id="examWrap">
    <div id="examHead">考场内容</div>
    <div id="examCon">
      <!-- Swiper -->
      <div class="swiper-container swiper-container-horizontal">
        <div class="swiper-wrapper" style="transition-duration: 0ms; transform: translate3d(0px, 0px, 0px);">
          <div class="swiper-slide swiper-slide-active" data-swiper-slide-index="0">
            
          </div>
          <div class="swiper-slide swiper-slide-next" data-swiper-slide-index="1">Slide 2</div>
          <div class="swiper-slide" data-swiper-slide-index="2">Slide 3</div>
          <div class="swiper-slide" data-swiper-slide-index="3">Slide 4</div>
          <div class="swiper-slide" data-swiper-slide-index="4">Slide 5</div>
          <div class="swiper-slide" data-swiper-slide-index="5">Slide 6</div>
          <div class="swiper-slide" data-swiper-slide-index="6">Slide 7</div>
          <div class="swiper-slide" data-swiper-slide-index="7">Slide 8</div>
          <div class="swiper-slide" data-swiper-slide-index="8">Slide 9</div>
          <div class="swiper-slide" data-swiper-slide-index="9">Slide 10</div>
        </div>
        <!-- Add Pagination -->
        <div class="swiper-pagination swiper-pagination-clickable swiper-pagination-bullets">
          <span class="swiper-pagination-bullet swiper-pagination-bullet-active" tabindex="0" role="button" aria-label="Go to slide 1">1</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 2">2</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 3">3</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 4">4</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 5">5</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 6">6</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 7">7</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 8">8</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 9">9</span>
          <span class="swiper-pagination-bullet" tabindex="0" role="button" aria-label="Go to slide 10">10</span>
        </div>
        <!-- Add Arrows -->
        <div class="swiper-button-next" tabindex="0" role="button" aria-label="Next slide"></div>
        <div class="swiper-button-prev" tabindex="0" role="button" aria-label="Previous slide"></div>
        <span class="swiper-notification" aria-live="assertive" aria-atomic="true"></span>
      </div>
    </div>
  </div>
</template>

<script>
import '@/../static/js/jquery-1.11.3.min.js'
import '@/../static/js/swiper-4.2.6.min.js'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted () {
    var swiper = new Swiper('.swiper-container', {
      slidesPerView: 1,
      spaceBetween: 10,
      loop: false,
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
        renderBullet: function (index, className) {
          return '<span class="' + className + '">' + (index + 1) + '</span>';
        }
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
  <style>
  html, body {
    position: relative;
    width: 100%;
    height: 100%;
  }
  body {
    font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
    font-size: 14px;
    color:#000;
    margin: 0;
    padding: 0;
  }
  #examWrap{
    width: 100%;
    height: 100%;
  }
  #examHead{
    height: 7%;
    line-height: 50px;
    text-align: center;
    font-size: 18px;
    border-bottom: 1px solid #ccc;
    box-sizing: border-box;
  }
  #examCon{
    height: 93%;
  }
  .swiper-container {
    width: 100%;
    height: 100%;
    margin-left: auto;
    margin-right: auto;
  }
  .swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center;
  }
  .swiper-pagination-bullet {
    width: 20px;
    height: 20px;
    text-align: center;
    line-height: 20px;
    font-size: 12px;
    color:#000;
    opacity: 1;
    background: rgba(0,0,0,0.2);
  }
  .swiper-pagination-bullet-active {
    color:#fff;
    background: #007aff;
  }
  </style>
