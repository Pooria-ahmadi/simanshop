<template>
  <div class="max-width-1160px mb-6">
    <div class="columns is-vcentered mt-6 has-text-centered-mobile mx-0">
      <div class="column is-5">
        <div>
          <img src="Asset 3@4x.png" alt="">
          <img src="Asset 2@4x.png" alt="">
          <img src="Asset 1@4x.png" alt="">
        </div>
        <h1 class="font-bold-number is-size-1-desktop is-size-4-mobile has-text-black">
          تولید و توزیع
        </h1>
        <h2 class="font-bold-number is-size-1-desktop is-size-4-mobile has-text-black">
          انواع مصالح ساختمانی
        </h2>
        <p>
          20 سال سابقه ی حضور و خدمت رسانی
        </p>
        <P>
          به مهندسین گرامی در صنعت ساخت و ساز
        </P>

        <div class="mt-4">
          <button class="button is-rounded is-black">
            محصولات
          </button>
          <button class="button is-rounded has-background-grey-lighter">
            ارتباط با ما
          </button>
        </div>
      </div>
      <div class="column has-text-centered">
        <img src="/siman.png" alt="">
      </div>
    </div>
    <p class="is-size-4 has-text-weight-bold has-text-black mt-6 has-text-centered-mobile">
      جدیدترین محصولات
    </p>
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
    <div class="columns is-multiline mx-0 mt-5">
      <div class="column is-one-quarter is-three-fifths-mobile has-text-centered" v-for="(image, index) in images"
        :key="index">
        <div class="image-container">
          <img :src="image.src" :alt="image.alt">
          <div class="corner-like has-background-black p-2">
            <img src="icons8-heart-30.png" alt="like">
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
          <img src="image 1.png" alt="">
        </div>
        <p class="has-text-grey-light text-decoration-line-grey has-text-centered">
          120,000
        </p>
        <button class="button is-black mt-4">
          افزودن به سبد خرید
        </button>
      </div>
    </div>
    <div class="columns mt-5 is-vcentered mx-0">
      <div class="column is-5">
        <p class="is-size-5 has-text-black has-text-weight-bold">
          سیمان چیست؟
        </p>
        <p class="mt-4 has-text-justified line-height-description">
          سیمان یک ماده پودری است که با افزودن آب تشکیل پسته‌ای سخت می‌دهد و برای ساخت سازه‌های ساختمانی استفاده می‌شود.
          این ماده به عنوان چسب و اتصال دهنده در بتن و ملات استفاده می‌شود و خواص فشاری بالایی دارد.
        </p>
      </div>
      <div class="column has-text-centered">
        <img src="AdobeStock_Preview 1.png" alt="">
      </div>
    </div>
    <p class="has-text-justified line-height-description mx-4">
      سیمان در بتن کاربرد دارد و وظیفه آن صرفا چسباندن دانه ها به یکدیگر است و به خودی خود تاثیری در مقاومت و باربری
      ندارد. از این رو بتن خوب بتنی است که وقتی نمونه ای از آن شکسته شود، دانه های سنگی آن از وسط شکسته شده و سیمان ها
      پاره نشود. سیمان ها دارای ریشه آهکی می باشند. به عبارت دیگر ماده اصلی سیمان و مواد تشکیل دهنده سیمان آهک و ماده
      اولیه اصلی تولید سیمان، سنگ آهک است. بر این اساس سیمان ترکیبی است از اکسید کلسیم (آهک) با سایر اکسیدها نظیر
      اکسید
      آلومینیوم، اکسید سیلیسیم، اکسید آهن، اکسید منیزیم و اکسید های قلیایی که میل ترکیب سیمان با آب داشته و در مجاورت
      هوا و در زیر آب به مرور سخت می گردد و دارای مقاومت می شود.
    </p>
    <div class="columns is-vcentered mt-6 has-text-centered-mobile mx-0">
      <div class="column is-5">
        <p class="is-size-5 has-text-black has-text-weight-bold mt-5">
          تیپ سیمان چیست؟
        </p>
        <p class="has-text-justified line-height-description mt-3">
          انواع سیمان از تیپ ۱ تا تیپ ۵ تقسیم بندی می شوند. بخش مهمی از تفاوت انواع تیپ سیمان با یکدیگر بر اساس زودگیر
          یا زودسخت بودن و میزان حرارتی است که به هنگام ترکیب آزاد می سازند. تقسیم بندی اصلی سیمان بر اساس نوع مواد
          اولیه آن به شکل پرتلند و غیرپرتلند خواهد بود. خط تولید سیمان پرتلند و تجهیزات مورد نیاز برای تولید انواع
          سیمان کاملا یکسان هستند. دلیل عمده ای که باعث تفاوت انواع تیپ سیمان می گردد، نوع مواد اولیه و درجه حرارت
          کوره در زمان تولید است. برای تولید سیمان پرتلند معمولی دمای کوره در حدود 1500 درجه خواهد بود. در ادامه به
          معرفی هر چه بهتر انواع سیمان می پردازیم.
        </p>
      </div>
      <div class="column has-text-centered">
        <img src="/siman5.png" alt="">
      </div>
    </div>
    <div class="has-background-grey-lighter full-width-background">
      <div class="max-width-1160px mx-auto">
        <div class="columns is-vcentered mt-6 has-text-centered-mobile mx-0 py-5">
          <div class="column has-text-centered is-5">
            <div class="is-relative">
              <img src="/siman6.png" alt="">
              <p class="text-on-img has-text-white has-text-weight-bold">
                انواع تیپ سیمان پرتلند:
              </p>
            </div>
          </div>
          <div class="column is-3 is-flex is-flex-direction-column is-align-items-center">
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند معمولی
              </p>
              <div class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 1
              </div>
            </div>
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند اصلاح شده 
              </p>
              <div class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 2
              </div>
            </div>
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند زود سخت شونده 
              </p>
              <div class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 3
              </div>
            </div>
          </div>
          <div class="column is-3 is-flex is-flex-direction-column is-align-items-center">
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند با حرارت کم 
              </p>
              <div class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                 تیپ 4
              </div>
            </div>
            <div class="box has-background-grey-lighter border-gret-dark border-radius-search-input-header is-relative">
              <p>
                سیمان پرتلند ضد سولفات 
              </p>
              <div class="title-type-siman has-text-black has-background-grey border-radius-search-input-header px-3 py-2">
                تیپ 5
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <p class="is-size-4 has-text-black has-text-weight-bold mt-5 mx-4">
      خرید سیمان
    </p>
    <div class="columns is-multiline mx-0 mt-5">
      <div class="column has-text-centered is-one-quarter is-three-fifths-mobile" v-for="(image, index) in images"
        :key="index">
        <div class="image-container">
          <img :src="image.src" :alt="image.alt">
          <div class="corner-like has-background-black p-2">
            <img src="icons8-heart-30.png" alt="like">
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
          <img src="image 1.png" alt="">
        </div>
        <p class="has-text-grey-light text-decoration-line-grey has-text-centered">
          120,000
        </p>
        <button class="button is-black mt-4">
          افزودن به سبد خرید
        </button>
      </div>
    </div>
    <div class="columns mt-3 is-vcentered mx-0">
      <div class="column is-5">
        <p class="is-size-5 has-text-black has-text-weight-bold">
          فروش سیمان در صنعت ساختمانی
        </p>
        <p class="mt-4 has-text-justified line-height-description">
          فروش سیمان به عنوان یکی از مهمترین محصولات در صنعت ساختمانی استراتژی‌های خاص خود را دارد. این صنعت تحت تأثیر
          عوامل اقتصادی، ساخت و ساز و تقاضای بازار قرار دارد. استراتژی‌های موفق فروش شامل تعیین قیمت مناسب، بازاریابی
          قوی، ارائه خدمات پس از فروش و برقراری روابط مؤثر با مشتریان و تأمین‌کنندگان است.
        </p>
        <p class="mt-4 has-text-justified line-height-description">
          فروش سیمان با قیمت مناسب می‌تواند به عنوان یک فرصت عالی برای ساخت و سازهای مختلف مورد استفاده قرار گیرد. این
          امر می‌تواند به کاهش هزینه‌های ساخت و اجرای پروژه‌ها کمک کند و باعث جذب بیشتر مشتریان شود.
        </p>
      </div>
      <div class="column has-text-centered">
        <img src="siman2.png" alt="">
      </div>
    </div>
    <p class="mt-4 mx-4 has-text-justified line-height-description">
      شرکت‌های فروش سیمان عموماً در تولید، بسته‌بندی و عرضه سیمان به بازارها مشغول هستند. آن‌ها معمولاً نقش اساسی در
      صنعت ساخت و ساز دارند و تأمین مواد اولیه برای پروژه‌های عظیم ساختمانی را بر عهده دارند. این شرکت‌ها باید با
      استانداردهای صنعتی، قوانین محیط زیست و نظارت‌های دولتی رعایت کنند.
    </p>
    <div class="is-relative">
      <div class="columns p-4 is-vcentered mx-0 img-background-shadow-black  border-radius-search-input-header mt-5">
        <div class="column is-5">
          <p class="mt-4 has-text-justified line-height-description has-text-black has-text-weight-bold">
            شرکت ما یکی از پیشگامان در صنعت فروش سیمان است. با بیش از دو دهه تجربه، ما به عنوان یک منبع قابل اعتماد برای
            تأمین سیمان با کیفیت و خدمات حرفه‌ای شناخته می‌شویم. تلاش ما بر این است که با ارائه محصولات با استانداردهای
            بالا و رضایت‌مندی مشتریان، در پروژه‌های ساختمانی و عمرانی نقش به‌سزای خود را ایفا کنیم.
          </p>
          <button class="mt-4 button is-rounded is-black">
            درباره ما
            <img src="arrow-left.png" alt="" class="mr-3">
          </button>
        </div>
        <div class="column has-text-centered">
          <img src="siman3.png" alt="">
        </div>
        <div class="rectangle"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      images: [
        { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000' },
        { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000' },
        { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000' },
        { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000' }
      ]
    }
  }
}
</script>
<style>
.img-background-shadow-black {
  background-image: url('/siman7.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

}
</style>
