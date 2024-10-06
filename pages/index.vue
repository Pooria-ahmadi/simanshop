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
      <div class="column is-one-quarter" v-for="(image, index) in images" :key="index">
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
    <div class="mx-4">
      <p class="has-text-justified line-height-description">
        سیمان در بتن کاربرد دارد و وظیفه آن صرفا چسباندن دانه ها به یکدیگر است و به خودی خود تاثیری در مقاومت و باربری
        ندارد. از این رو بتن خوب بتنی است که وقتی نمونه ای از آن شکسته شود، دانه های سنگی آن از وسط شکسته شده و سیمان ها
        پاره نشود. سیمان ها دارای ریشه آهکی می باشند. به عبارت دیگر ماده اصلی سیمان و مواد تشکیل دهنده سیمان آهک و ماده
        اولیه اصلی تولید سیمان، سنگ آهک است. بر این اساس سیمان ترکیبی است از اکسید کلسیم (آهک) با سایر اکسیدها نظیر
        اکسید
        آلومینیوم، اکسید سیلیسیم، اکسید آهن، اکسید منیزیم و اکسید های قلیایی که میل ترکیب سیمان با آب داشته و در مجاورت
        هوا و در زیر آب به مرور سخت می گردد و دارای مقاومت می شود.
      </p>
      <p class="is-size-5 has-text-black has-text-weight-bold mt-5">
        سیمان چیست؟
      </p>
      <p class="mt-4 has-text-justified line-height-description">
        سیمان یک ماده پودری است که با افزودن آب تشکیل پسته‌ای سخت می‌دهد و برای ساخت سازه‌های ساختمانی استفاده می‌شود.
        این ماده به عنوان چسب و اتصال دهنده در بتن و ملات استفاده می‌شود و خواص فشاری بالایی دارد.
      </p>
      <p class="mt-4">
        انواع تیپ سیمان پرتلند:
      </p>
      <ul class="mt-4 list-style-type-disc pr-5">
        <li>سیمان پرتلند معمولی به عنوان سیمان تیپ ۱</li>
        <li>سیمان پرتلند اصلاح شده به عنوان سیمان تیپ ۲</li>
        <li>سیمان پرتلند زود سخت شونده به عنوان سیمان تیپ ۳</li>
        <li>سیمان پرتلند با حرارت کم به عنوان سیمان تیپ ۴</li>
        <li>سیمان پرتلند ضد سولفات بانوان سیمان تیپ ۵</li>
      </ul>
    </div>
    <p class="is-size-4 has-text-black has-text-weight-bold mt-5 mx-4">
      خرید سیمان
    </p>
    <div class="columns is-multiline mx-0 mt-5">
      <div class="column is-one-quarter" v-for="(image, index) in images" :key="index">
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
    <div class="columns mt-3 is-vcentered mx-0">
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
