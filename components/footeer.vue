<template>
  <section>
    <div class="has-background-primary-dark" :class="{ 'phone-image ': true, 'animate': animate }">
      <a href="tel:09121472031">
        <img src="icons8-phone-33.png" alt="پشتیبانی" class="p-3" />
      </a>
    </div>
    <div class="is-relative">
      <img src="footer.png" alt="" class="background-image">
      <div class="columns has-text-centered mx-auto position-absolute-text-about-we is-vcentered">
        <div class="column">
          <div class="is-flex is-align-items-center is-justify-content-center">
            <img src="icon-siman.png" alt="">
            <p class="pr-2 has-text-white has-text-weight-bold pt-5">
              پارسیان سازه
            </p>
          </div>
          <div class="my-4">
            <a href="https://www.instagram.com/parsiansazeh_co?igsh=MTZ4NXU2dXBlN3lsbQ==" target="_blank">
              <img src="black-instagram-logo-3497.png" alt="اینستاگرام سیمان شاپ">
            </a>
            <a href="https://wa.me/09121472031" class="px-4" target="_blank">
              <img src="whatsapp-logo-4453.png" alt="واتساپ سیمان شاپ">
            </a>
            <img src="facebook-logo-108.png" alt="">
          </div>
          <a class="has-text-grey-dark" href="tel:09121472031">
            شماره تماس 09121472031
          </a>
          <p>
            با مدیریت جعفری
          </p>
        </div>
        <div class="column">
          <NuxtLink to="/Contactus" class="has-text-grey-dark">
            <p>
              ارتباط با ما
            </p>
          </NuxtLink>
          <a class="has-text-grey-dark" href="/">
            <p class="mt-3">
              سوالات متدوال
            </p>
          </a>
          <a class="has-text-grey-dark" href="/">
            <p class="mt-3">
              تیم ما
            </p>
          </a>
          <NuxtLink to="/aboutus" class="has-text-grey-dark">
            <p class="mt-3">
              درباره ما
            </p>
          </NuxtLink>
        </div>
        <div class="column">
          <a class="has-text-grey-dark" href="/">
            <p>
              نحوه ثبت سفارش
            </p>
          </a>
          <a class="has-text-grey-dark" href="/">
            <p class="mt-3">
              شیوه های پرداخت
            </p>
          </a>
          <a class="has-text-grey-dark" href="/">
            <p class="mt-3">
              پشتیبانی
            </p>
          </a>
          <NuxtLink class="has-text-grey-dark" to="/rules">
            <p class="mt-3">
              قوانین و مقررات
            </p>
          </NuxtLink>
        </div>
        <div class="column is-4">
          <p class="has-text-white is-size-4">
            همراه شما هستیم تا پایان کار!
          </p>
          <p class="mt-5">
            سه راه تهرانپارس، روبروی ترمینال شرق
          </p>
          <p class="my-2">
            ۷ روز هفته، ۲۴ ساعته پاسخگوی شما هستیم
          </p>
          <p>
            © تمام حقوق برای siamnshop.ir محفوظ است
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      animate: true
    };
  },
  mounted() {
    setTimeout(() => {
      this.animate = false;
    }, 10000);
  }
}
</script>
<style>
.phone-image {
  position: fixed;
  bottom: 20px;
  left: 27px;
  width: 60px;
  border-radius: 50px;
  height: 60px;
}

.phone-image.animate {
  animation: bounce 2s infinite;
}
</style>