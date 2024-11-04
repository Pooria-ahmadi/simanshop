<template>
  <div class="my-6 py-3 ">
    <div class="max-width-1160px ">
      <div class="columns is-vcentered py-6 px-4 has-text-centered-mobile mx-0 is-rounded-five mt-5" :class="slide.bgcolor" v-for="(slide, index) in slides" :key="index" v-show="index === currentSlide">
        <div class="column is-5">
          <div>
            <img src="siman10.png" alt="وسایل مورد نیاز برای مصالح ساختمانی">
            <img src="siman9.png" alt="وسایل مورد نیاز برای مصالح ساختمانی">
            <img src="siman8.png" alt="وسایل مورد نیاز برای مصالح ساختمانی">
          </div>
          <h1 :class="slide.color" class="font-bold-number is-size-1-desktop is-size-4-mobile">
            {{ slide.caption }}
          </h1>
          <h2 :class="slide.color" class="font-bold-number is-size-1-desktop is-size-4-mobile">
            {{slide.subtittle }}
          </h2>
          <p>
            {{ slide.subtittle2 }}
          </p>
          <P>
            {{slide.subtittle3 }}
          </P>
          <div class="mt-4">
            <button class="button is-rounded ":class="slide.colorbutton2">
              محصولات
            </button>
            <NuxtLink to="/Contactus">
              <button class="button is-rounded  mr-4" :class="slide.colorbutton">
                ارتباط با ما
              </button>
            </NuxtLink>
          </div>
        </div>
        <div class="column has-text-centered">
          <img :src="slide.image2" alt=" تولید و توزیع مصالح ساختمانی">
        </div>
        <a class="next has-text-weight-bold is-size-1-desktop is-size-4-mobile has-text-grey-darker" @click="prevSlide">&#10094;</a>
        <a class="prev has-text-weight-bold is-size-1-desktop is-size-4-mobile has-text-grey-darker" @click="nextSlide">&#10095;</a>
      </div>
      <div class="has-text-centered mb-4 mx-0">
      <span v-for="(dot, index) in slides" :key="index" class="dot" :class="{ 'active': index === currentSlide }"
        @click="changeSlide(index)"></span>
    </div>
      <h3 class="is-size-4 has-text-weight-bold has-text-black mt-6 has-text-centered-mobile">
        جدیدترین محصولات
      </h3>
      <div class="is-flex justify-content-center-mobile mt-5">
        <p class="has-text-black is-underlined">
          تخفیف دار
        </p>
        <p class="mx-4">
          ارزان ترین
        </p>
        <p>
          گران ترین
        </p>
      </div>
      <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
        <div class="column has-text-centered is-one-quarter is-three-fifths-mobile" v-for="(image, index) in images"
          :key="index">

          <div class="image-container">
            <NuxtLink to="/product">
              <img :src="image.src" :alt="image.alt">
            </NuxtLink>
            <div v-if="image.showlike" class="corner-like has-background-black p-2" @click="activelike(index)">
              <img src="icons8-heart-30.png" alt="like">
            </div>
            <div v-else class="corner-like has-background-black p-2" @click="activelike(index)">
              <img src="icons8-like-20.png" alt="like">
            </div>
          </div>

          <p class="has-text-centered mt-4 has-text-black">{{ image.caption }}</p>
          <div class="is-flex is-align-items-center is-justify-content-center mt-2">
            <p class="has-text-danger is-size-7">
              3%
            </p>
            <p class="mx-2">
              {{ image.price }}
            </p>
            <img src="image 1.png" alt="مبلغ">
          </div>
          <p class="has-text-grey-light text-decoration-line-grey has-text-centered">
            120,000
          </p>
          <button v-if="!image.showCart" class="button is-black mt-4" @click="toggleCart(index)">
            افزودن به سبد خرید
          </button>
          <div v-else class="is-flex is-align-items-center is-justify-content-center mt-3">
            <button class="px-4 py-2 button is-black" @click="increment(index)">
              +
            </button>
            <input type="text" class="mx-2 has-text-centered" style="width: 35px;" :value="image.number">
            <button class="px-4 py-2 button is-light" @click="decrement(index)">
              -
            </button>
          </div>
        </div>
      </div>
      <div class="columns mt-5 is-vcentered mx-0" data-aos="fade-right" data-aos-offset="300"
        data-aos-easing="ease-in-sine">
        <div class="column is-5 px-5">
          <h2 class="is-size-5 has-text-black has-text-weight-bold">
            سیمان چیست؟
          </h2>
          <p class="mt-4 has-text-justified line-height-description">
            سیمان یک ماده پودری است که با افزودن آب تشکیل پسته‌ای سخت می‌دهد و برای ساخت سازه‌های ساختمانی استفاده
            می‌شود.
            این ماده به عنوان چسب و اتصال دهنده در بتن و ملات استفاده می‌شود و خواص فشاری بالایی دارد.
          </p>
        </div>
        <div class="column has-text-centered">
          <img src="AdobeStock_Preview 1.png" alt="سیمان چیست">
        </div>
      </div>
      <p class="has-text-justified line-height-description px-5" data-aos="zoom-out">
        سیمان در بتن کاربرد دارد و وظیفه آن صرفا چسباندن دانه ها به یکدیگر است و به خودی خود تاثیری در مقاومت و باربری
        ندارد. از این رو بتن خوب بتنی است که وقتی نمونه ای از آن شکسته شود، دانه های سنگی آن از وسط شکسته شده و سیمان ها
        پاره نشود. سیمان ها دارای ریشه آهکی می باشند. به عبارت دیگر ماده اصلی سیمان و مواد تشکیل دهنده سیمان آهک و ماده
        اولیه اصلی تولید سیمان، سنگ آهک است. بر این اساس سیمان ترکیبی است از اکسید کلسیم (آهک) با سایر اکسیدها نظیر
        اکسید
        آلومینیوم، اکسید سیلیسیم، اکسید آهن، اکسید منیزیم و اکسید های قلیایی که میل ترکیب سیمان با آب داشته و در مجاورت
        هوا و در زیر آب به مرور سخت می گردد و دارای مقاومت می شود.
      </p>

      <div class="columns is-vcentered mt-6 has-text-centered-mobile mx-0" v-if="cementInfo" data-aos="fade-right"
        data-aos-offset="300" data-aos-easing="ease-in-sine">
        <div class="column is-5 px-5">
          <h2 class="is-size-5 has-text-black has-text-weight-bold mt-5">{{ cementInfo.title }}</h2>
          <p class="has-text-justified line-height-description mt-3">{{ cementInfo.description }}</p>
        </div>
        <div class="column has-text-centered">
          <img :src="cementInfo.imageUrl" :alt="cementInfo.title" />
        </div>
      </div>
    </div>
    <div class="has-background-grey-lighter full-width-background">
      <div class="max-width-1160px mx-auto">
        <div class="columns is-vcentered mt-6 has-text-centered-mobile mx-0 py-5">
          <div class="column has-text-centered is-5">
            <div class="is-relative">
              <img src="/siman6.png" alt="انواع تیپ سیمان پرتلند">
              <h2 class="text-on-img has-text-white has-text-weight-bold">
                انواع تیپ سیمان پرتلند:
              </h2>
            </div>
          </div>
          <div class="column is-3 is-flex is-flex-direction-column is-align-items-center">
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند معمولی
              </p>
              <div
                class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 1
              </div>
            </div>
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند اصلاح شده
              </p>
              <div
                class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 2
              </div>
            </div>
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند زود سخت شونده
              </p>
              <div
                class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 3
              </div>
            </div>
          </div>
          <div class="column is-3 is-flex is-flex-direction-column is-align-items-center">
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند با حرارت کم
              </p>
              <div
                class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 4
              </div>
            </div>
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند ضد سولفات
              </p>
              <div
                class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 5
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="max-width-1160px ">
      <p class="is-size-4 has-text-black has-text-weight-bold mt-5 mx-4">
        خرید سیمان
      </p>
      <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
        <div class="column has-text-centered is-one-quarter is-three-fifths-mobile" v-for="(image, index) in images"
          :key="index">
          <div class="image-container">
            <NuxtLink to="/product">
              <img :src="image.src" :alt="image.alt">
            </NuxtLink>
            <div v-if="image.showlike" class="corner-like has-background-black p-2" @click="activelike(index)">
              <img src="icons8-heart-30.png" alt="like">
            </div>
            <div v-else class="corner-like has-background-black p-2" @click="activelike(index)">
              <img src="icons8-like-20.png" alt="like">
            </div>
          </div>
          <p class="has-text-centered mt-4 has-text-black">{{ image.caption }}</p>
          <div class="is-flex is-align-items-center is-justify-content-center mt-2">
            <p class="has-text-danger is-size-7">
              3%
            </p>
            <p class="mx-2">
              {{ image.price }}
            </p>
            <img src="image 1.png" alt="مبلغ">
          </div>
          <p class="has-text-grey-light text-decoration-line-grey has-text-centered">
            120,000
          </p>
          <button v-if="!image.showCart" class="button is-black mt-4" @click="toggleCart(index)">
            افزودن به سبد خرید
          </button>
          <div v-else class="is-flex is-align-items-center is-justify-content-center mt-3">
            <button class="px-4 py-2 button is-black" @click="increment(index)">
              +
            </button>
            <input type="text" class="mx-2 has-text-centered" style="width: 35px;" :value="image.number">
            <button class="px-4 py-2 button is-light" @click="decrement(index)">
              -
            </button>
          </div>
        </div>
      </div>
      <p class="is-size-4 has-text-black has-text-weight-bold mt-5 mx-4">
        خرید گچ
      </p>
      <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
        <div class="column has-text-centered is-one-quarter is-three-fifths-mobile" v-for="(image, index) in images"
          :key="index">
          <div class="image-container">
            <NuxtLink to="/product">
              <img :src="image.src" :alt="image.alt">
            </NuxtLink>
            <div v-if="image.showlike" class="corner-like has-background-black p-2" @click="activelike(index)">
              <img src="icons8-heart-30.png" alt="like">
            </div>
            <div v-else class="corner-like has-background-black p-2" @click="activelike(index)">
              <img src="icons8-like-20.png" alt="like">
            </div>
          </div>
          <p class="has-text-centered mt-4 has-text-black">{{ image.caption }}</p>
          <div class="is-flex is-align-items-center is-justify-content-center mt-2">
            <p class="has-text-danger is-size-7">
              3%
            </p>
            <p class="mx-2">
              {{ image.price }}
            </p>
            <img src="image 1.png" alt="مبلغ">
          </div>
          <p class="has-text-grey-light text-decoration-line-grey has-text-centered">
            120,000
          </p>
          <button v-if="!image.showCart" class="button is-black mt-4" @click="toggleCart(index)">
            افزودن به سبد خرید
          </button>
          <div v-else class="is-flex is-align-items-center is-justify-content-center mt-3">
            <button class="px-4 py-2 button is-black" @click="increment(index)">
              +
            </button>
            <input type="text" class="mx-2 has-text-centered" style="width: 35px;" :value="image.number">
            <button class="px-4 py-2 button is-light" @click="decrement(index)">
              -
            </button>
          </div>
        </div>
      </div>
      <p class="is-size-4 has-text-black has-text-weight-bold mt-5 mx-4">
        خرید بلوک
      </p>
      <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
        <div class="column has-text-centered is-one-quarter is-three-fifths-mobile" v-for="(image, index) in images"
          :key="index">
          <div class="image-container">
            <NuxtLink to="/product">
              <img :src="image.src" :alt="image.alt">
            </NuxtLink>
            <div v-if="image.showlike" class="corner-like has-background-black p-2" @click="activelike(index)">
              <img src="icons8-heart-30.png" alt="like">
            </div>
            <div v-else class="corner-like has-background-black p-2" @click="activelike(index)">
              <img src="icons8-like-20.png" alt="like">
            </div>
          </div>
          <p class="has-text-centered mt-4 has-text-black">{{ image.caption }}</p>
          <div class="is-flex is-align-items-center is-justify-content-center mt-2">
            <p class="has-text-danger is-size-7">
              3%
            </p>
            <p class="mx-2">
              {{ image.price }}
            </p>
            <img src="image 1.png" alt="مبلغ">
          </div>
          <p class="has-text-grey-light text-decoration-line-grey has-text-centered">
            120,000
          </p>
          <button v-if="!image.showCart" class="button is-black mt-4" @click="toggleCart(index)">
            افزودن به سبد خرید
          </button>
          <div v-else class="is-flex is-align-items-center is-justify-content-center mt-3">
            <button class="px-4 py-2 button is-black" @click="increment(index)">
              +
            </button>
            <input type="text" class="mx-2 has-text-centered" style="width: 35px;" :value="image.number">
            <button class="px-4 py-2 button is-light" @click="decrement(index)">
              -
            </button>
          </div>
        </div>
      </div>
      <p class="mt-4 px-5 has-text-justified line-height-description" data-aos="zoom-out-right">
        شرکت‌های فروش سیمان عموماً در تولید، بسته‌بندی و عرضه سیمان به بازارها مشغول هستند. آن‌ها معمولاً نقش اساسی در
        صنعت ساخت و ساز دارند و تأمین مواد اولیه برای پروژه‌های عظیم ساختمانی را بر عهده دارند. این شرکت‌ها باید با
        استانداردهای صنعتی، قوانین محیط زیست و نظارت‌های دولتی رعایت کنند.
      </p>
      <div class="is-relative">
        <div class="columns p-4 is-vcentered mx-0 img-background-shadow-black  border-radius-search-input-header mt-5">
          <div class="column is-5 px-5">
            <p class="mt-4 has-text-justified line-height-description has-text-white has-text-weight-bold">
              شرکت ما یکی از پیشگامان در صنعت فروش سیمان است. با بیش از دو دهه تجربه، ما به عنوان یک منبع قابل اعتماد
              برای
              تأمین سیمان با کیفیت و خدمات حرفه‌ای شناخته می‌شویم. تلاش ما بر این است که با ارائه محصولات با
              استانداردهای
              بالا و رضایت‌مندی مشتریان، در پروژه‌های ساختمانی و عمرانی نقش به‌سزای خود را ایفا کنیم.
            </p>
            <button class="mt-4 button is-rounded has-text-white backgrond-color-C6C6C691">
              درباره ما
              <img src="arrow-left.png" class="mr-3">
            </button>
          </div>
          <NuxtLink to="/aboutus">
            <div class="column has-text-centered">
            <img src="siman3.png" alt="درباره ما">
          </div>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: 'سیمان شاپ',
    }
  },
  data() {
    return {
      currentSlide: 0,
      slides: [
        {bgcolor:"has-background-white", image2:'/siman.png', caption: 'تولید و توزیع', subtittle: 'انواع مصالح ساختمانی', subtittle2: '20 سال سابقه ی حضور و خدمت رسانی', subtittle3: 'به مهندسین گرامی در صنعت ساخت و ساز', color: 'has-text-black', colorbutton: 'has-background-grey-lighter',colorbutton2: 'is-black' },
        {bgcolor:"has-background-black", image2:'/siman.png', caption: ' تولید و توزیع', subtittle: 'انواع مصالح ساختمانی', subtittle2: '20 سال سابقه ی حضور و خدمت رسانی', subtittle3: 'به مهندسین گرامی در صنعت ساخت و ساز', color: 'has-text-white', colorbutton: 'has-background-grey-lighter',colorbutton2: '' },
      ],
      images: [
        { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false, showlike: true },
        { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false, showlike: true },
        { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false, showlike: true },
        { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false, showlike: true }
      ],
      cementInfo: null,
    }
  },
  mounted() {
    this.fetchCementInfo();
  },
  methods: {
    showSlides() {
      setInterval(() => {
        this.currentSlide = (this.currentSlide + 1) % this.slides.length;
      }, 5000);
    },
    changeSlide(index) {
      this.currentSlide = index;
    },
    prevSlide() {
      this.currentSlide = (this.currentSlide - 1 + this.slides.length) % this.slides.length;
    },
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.slides.length;
    },
    fetchCementInfo() {
      this.$axios
        .get('https://fapi.simanshop.com/cement-info')
        .then(response => {
          this.cementInfo = response.data;
        })
        .catch(error => {
          console.error('Error fetching cement info:', error);
        });
    },
    activelike(index) {
      this.images[index].showlike = !this.images[index].showlike
    },
    toggleCart(index) {
      this.$set(this.images, index, {
        ...this.images[index],
        showCart: !this.images[index].showCart
      });
    },
    increment(index) {
      this.$set(this.images, index, {
        ...this.images[index],
        number: this.images[index].number + 1
      });
    },
    decrement(index) {
      if (this.images[index].number > 0) {
        this.$set(this.images, index, {
          ...this.images[index],
          number: this.images[index].number - 1
        });
      }
    }
  },
}
</script>
<style>
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 335px;
  width: auto;
  padding: 35px;
  margin-top: -45px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
}

.prev {
  left: 0;
  border-radius: 3px 0 0 3px;
}
.img-background-shadow-black {
  background-image: url('/siman3333.png');
  background-size: cover;
  background-position: center;

}

.overflow-x-auto {
  overflow-x: auto;
}

.backgrond-color-C6C6C691 {
  background-color: #C6C6C691;
}
</style>
