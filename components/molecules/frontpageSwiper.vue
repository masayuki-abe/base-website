<template>
  <swiper
    :options="swiperOption"
    :class="className"
  >
    <swiper-slide>
      <img src="https://source.unsplash.com/0cZgvYHirBg" width="1080" height="720">
    </swiper-slide>
    <swiper-slide>
      <img src="https://source.unsplash.com/7RWBSYA9Rro" width="1080" height="720">
    </swiper-slide>
    <swiper-slide>
      <img src="https://source.unsplash.com/_UeY8aTI6d0" width="1080" height="720">
    </swiper-slide>
  </swiper>
</template>

<script>
export default {
  data() {
    return {
      swiperOption: {
        speed: 1000,
        autoplay: {
          delay: 2500,
          disableOnInteraction: false,
        },
        slidesPerView: 1,
        loop: true,
      },
    }
  },
  props: {
    className: {
      type: String,
    }
  },
}
</script>