<template>
  <section>
    <div class="has-background-primary-dark" :class="{ 'phone-image ': true, 'animate': animate }">
      <a href="tel:09121472031">
        <img src="icons8-phone-33.png" alt="پشتیبانی" class="p-3" />
      </a>
    </div>
    <div class="bg-container is-flex is-justify-content-center">
      <div
        class="columns mb-0 columns-m-flex-direction has-text-centered mx-auto is-flex is-align-items-center is-justify-content-center content-container py-6">
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
          </div>
          <a class="has-text-grey" href="tel:09121472031">
            شماره تماس 09121472031
          </a>
          <p class="has-text-grey">
            با مدیریت جعفری
          </p>
        </div>
        <div class="column">
          <NuxtLink to="/Contactus" class="has-text-grey">
            <p>
              ارتباط با ما
            </p>
          </NuxtLink>
          <a class="has-text-grey" href="/">
            <p class="mt-3">
              سوالات متدوال
            </p>
          </a>
          <a class="has-text-grey" href="/">
            <p class="mt-3">
              تیم ما
            </p>
          </a>
          <NuxtLink to="/aboutus" class="has-text-grey">
            <p class="mt-3">
              درباره ما
            </p>
          </NuxtLink>
        </div>
        <div class="column">
          <a class="has-text-grey" href="/">
            <p>
              نحوه ثبت سفارش
            </p>
          </a>
          <a class="has-text-grey" href="/">
            <p class="mt-3">
              شیوه های پرداخت
            </p>
          </a>
          <a class="has-text-grey" href="/">
            <p class="mt-3">
              پشتیبانی
            </p>
          </a>
          <NuxtLink class="has-text-grey" to="/rules">
            <p class="mt-3">
              قوانین و مقررات
            </p>
          </NuxtLink>
        </div>
        <div class="column is-4">
          <p class="has-text-white is-size-4">
            همراه شما هستیم تا پایان کار!
          </p>
          <p class="mt-5 has-text-grey">
            خیابان دماوند - روبروی ترمینال شرق - نبش خیابان باقر آذری - پلاک 283 - طبقه اول - واحد 1
          </p>
          <p class="my-2 has-text-grey">
            ۷ روز هفته، ۲۴ ساعته پاسخگوی شما هستیم
          </p>
          <p class="has-text-grey">
            © تمام حقوق برای simanshop.ir محفوظ است
          </p>
        </div>
        <div class="column">
          <a referrerpolicy="origin" target="_blank"
            href="https://trustseal.enamad.ir/?id=541280&amp;Code=Hoe3799d6k91VZEjbpExztMe64YN7ttG"><img
              referrerpolicy="origin"
              src="https://trustseal.enamad.ir/logo.aspx?id=541280&amp;Code=Hoe3799d6k91VZEjbpExztMe64YN7ttG" alt=""
              code="Hoe3799d6k91VZEjbpExztMe64YN7ttG" style="cursor:pointer"></a>
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
@media (max-width: 768px) {
  .columns-m-flex-direction {
    flex-direction: column;
  }
}

.bg-container {
  background-image: url('/footer.png');
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
}

.content-container {
  max-width: 1160px;
  width: 100%;
}

.phone-image {
  position: fixed;
  bottom: 20px;
  left: 27px;
  width: 60px;
  border-radius: 50px;
  height: 60px;
  z-index: 1000;
}

.phone-image.animate {
  animation: bounce 2s infinite;
}
</style>