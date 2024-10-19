<template>
    <div class="max-width-1160px my-6 py-3">

        <div class="columns mx-0 mt-5 is-vcentered">
            <div class="column has-text-centered ">



                <div v-for="(slide, index) in slides" :key="index" v-show="index === currentSlide">
                    <div class="test is-relative has-background-black p-2 mr-6">
                        <img src="icons8-heart-30.png" alt="like">
                    </div>
                    <div>
                        <img :src="slide.image" :alt="slide.alt">
                    </div>
                </div>
                <div class="has-text-centered mb-4 mx-0">
                    <span v-for="(dot, index) in slides" :key="index" class="dot"
                        :class="{ 'active': index === currentSlide }" @click="changeSlide(index)"></span>
                </div>
            </div>
            <!-- for not active -->
            <div v-if="falseshow" class="column img-background-black border-radius-button mx-2">
                <div class="columns mx-0 is-centered py-5">
                    <div class="column is-10">
                        <div class="is-flex is-justify-content-space-between is-align-items-center">
                            <div class="has-text-grey-light">
                                سیمان
                            </div>
                            <div>
                                <img src="Group 52.png" alt="" @click="activebutton">
                            </div>
                        </div>
                        <p class="is-size-3 has-text-white">
                            سیمان تیپ 2 پنجاه کیلویی
                        </p>
                        <div class="is-flex is-align-items-center mt-2">
                            <p class="has-text-grey-light text-decoration-line-grey has-text-centered">
                                120,000
                            </p>
                            <p class="color-red is-size-7 mr-3">
                                3%
                            </p>
                        </div>
                        <div class="is-flex is-align-items-center">
                            <p class="ml-2 is-size-4 has-text-white">
                                150،000
                            </p>
                            <img src="image 1.png" alt="مبلغ">
                        </div>
                        <div class="is-flex is-align-items-center mt-5">
                            <p class="ml-4 has-text-grey-lighter">
                                توضیحات
                            </p>
                            <p class="has-text-grey">
                                ویژگی ها
                            </p>
                        </div>
                        <div class="is-relative">
                            <hr class="mt-3 has-background-grey-darker">
                            <hr class="white-hr has-background-grey-light">
                        </div>
                        <p class="has-text-grey-light has-text-justified line-height-description">
                            لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است
                            چاپگرها و متون بلکه روزنامه و مجله در ستون و سطر آنچنا که لازم است و برای شرایط فعلی
                            تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد کتابهای زیادی در
                            شصت و سه درصد گذشته حال و آینده شناخت فراوان جامعه و متخصصان را می طلبد تا با نرم افزارها
                            شناخت بیشتری را برای طراحان رایانه ای علی الخصوص طراحان خلاقی و فرهنگ پیشرو در زبان فارسی
                            ایجاد کرد
                        </p>
                        <div class="is-flex mt-6 is-align-items-center">
                            <div>
                                <p class="has-text-white ">
                                    تعداد
                                </p>
                                <div
                                    class="is-flex background-black-input p-1 border-radius mt-3 is-align-items-center has-background-black-ter">
                                    <p class="has-text-grey-lighter px-3" @click="incrementnumber">
                                        +
                                    </p>
                                    <p class="px-4 has-text-grey-lighter">
                                        {{ number }}
                                    </p>
                                    <p class="has-text-grey-lighter px-3" @click="decrementnumber">
                                        -
                                    </p>
                                </div>
                            </div>
                            <div class="mr-5">
                                <p class="has-text-white ">
                                    مجموع قیمت
                                </p>
                                <div
                                    class="is-flex background-black p-1 border-radius mt-3 is-align-items-center has-background-black-ter">
                                    <p class="has-text-grey-lighter px-1">
                                        115،000 تومان
                                    </p>
                                </div>
                            </div>
                        </div>
                        <button
                            class="button is-responsive width-432px is-rounded is-flex is-justify-content-center is-align-items-center mt-5">
                            <div class="has-text-white is-flex-grow-1 is-size-6-mobile">
                                افزودن به سبد خرید
                            </div>
                            <div class="pt-1">
                                <img src="basket.png" alt="">
                            </div>
                        </button>

                    </div>
                </div>
            </div>

            <!-- for active -->

            <div v-else class="column back-color-F8F8F8 border-radius-button mx-2">
                <div class="columns mx-0 is-centered py-5">
                    <div class="column is-10">
                        <div class="is-flex is-justify-content-space-between is-align-items-center">
                            <div class="has-text-black">
                                سیمان
                            </div>
                            <div @click="activebutton">
                                <img src="active.png" alt="">
                            </div>
                        </div>
                        <p class="is-size-3 has-text-black">
                            سیمان تیپ 2 پنجاه کیلویی
                        </p>
                        <div class="is-flex is-align-items-center mt-2">
                            <p class="has-text-black text-decoration-line-grey has-text-centered">
                                120,000
                            </p>
                            <p class="color-red is-size-7 mr-3">
                                3%
                            </p>
                        </div>
                        <div class="is-flex is-align-items-center">
                            <p class="ml-2 is-size-4 has-text-black">
                                150،000
                            </p>
                            <img src="image 1.png" alt="مبلغ">
                        </div>
                        <div class="is-flex is-align-items-center mt-5">
                            <div class="is-relative is-inline-block">
                                <p class="has-text-black has-text-weight-bold">
                                    توضیحات
                                    <hr class=" has-background-black my-0">
                                </p>
                            </div>

                            <p class="has-text-black mr-4 mb-1">
                                ویژگی ها
                            </p>
                        </div>



                        <p class="has-text-black has-text-justified line-height-description mt-3">
                            لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است
                            چاپگرها و متون بلکه روزنامه و مجله در ستون و سطر آنچنا که لازم است و برای شرایط فعلی
                            تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد کتابهای زیادی در
                            شصت و سه درصد گذشته حال و آینده شناخت فراوان جامعه و متخصصان را می طلبد تا با نرم افزارها
                            شناخت بیشتری را برای طراحان رایانه ای علی الخصوص طراحان خلاقی و فرهنگ پیشرو در زبان فارسی
                            ایجاد کرد
                        </p>
                        <div class="is-flex mt-6 is-align-items-center">
                            <div>
                                <p class="has-text-black ">
                                    تعداد
                                </p>
                                <div
                                    class="border-grey is-flex background-black-input p-1 border-radius mt-3 is-align-items-center has-background-grey-lighter">
                                    <p class="has-text-black px-3" @click="incrementnumber">
                                        +
                                    </p>
                                    <p class="px-4 has-text-black">
                                        {{ number }}
                                    </p>
                                    <p class="has-text-black px-3" @click="decrementnumber">
                                        -
                                    </p>
                                </div>
                            </div>
                            <div class="mr-5">
                                <p class="has-text-black ">
                                    مجموع قیمت
                                </p>
                                <div class="p-1 border-radius mt-3 has-background-grey-lighter">
                                    <p class="px-1 has-text-black">
                                        115،000 تومان
                                    </p>
                                </div>
                            </div>
                        </div>
                        <button
                            class="button is-responsive width-432px is-rounded is-flex is-justify-content-center is-align-items-center mt-5 has-background-black">
                            <div class="has-text-white is-flex-grow-1 is-size-6-mobile">
                                افزودن به سبد خرید
                            </div>
                            <div class="pt-1">
                                <img src="basket.png" alt="">
                            </div>
                        </button>

                    </div>
                </div>
            </div>
        </div>
        <p class="is-size-4 has-text-black mt-6 font-bold-number mr-6">
            نظرات کاربران
        </p>
        <div class="columns is-vcentered mt-5 mx-0">
            <div class="column">
                <div class="is-flex justify-content-center-mobile">
                    <p class="has-text-black is-underlined">
                        تخفیف دار
                    </p>
                    <p class="mx-5">
                        ارزان ترین
                    </p>
                    <p>
                        گران ترین
                    </p>
                </div>
            </div>
            <div class="column is-hidden-mobile">
                <div class="is-flex is-justify-content-left is-align-items-center">
                    <button class="button is-black has-text-white">
                        افزودن نظر +
                    </button>
                    <p class="mx-5">
                        دو دیدگاه
                    </p>
                </div>
            </div>
        </div>
        <div class="columns mx-0 is-vcentered">
            <div class="column">
                <div class="box width-550px has-background-grey-lighter is-hidden-mobile">
                    <div class="is-flex is-align-items-center">
                        <p class=" has-text-grey">
                            ناشناس
                        </p>
                        <span class="dot-small mr-2 has-background-grey"></span>
                        <p class="mr-2 has-text-grey">
                            2 روز پیش
                        </p>
                    </div>
                    <p class="my-2 has-text-black">
                        خوب هست پیشنهاد میکنم!
                    </p>
                    <p class="has-text-justified">
                        لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است
                        چاپگرها و متون بلکه روزنامه و مجله در ستون و سطر آنچنا که لازم است.
                    </p>
                    <div class="has-text-left">
                        <img src="Like.png" alt="" class="mr-4">
                        <img src="Dislike.png" alt="" class="mr-3">
                    </div>
                </div>
                <div class="box has-background-grey-lighter is-hidden-desktop">
                    <div class="is-flex is-align-items-center">
                        <p class=" has-text-grey">
                            ناشناس
                        </p>
                        <span class="dot-small mr-2 has-background-grey"></span>
                        <p class="mr-2 has-text-grey">
                            2 روز پیش
                        </p>
                    </div>
                    <p class="my-2 has-text-black">
                        خوب هست پیشنهاد میکنم!
                    </p>
                    <p class="has-text-justified">
                        لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است
                        چاپگرها و متون بلکه روزنامه و مجله در ستون و سطر آنچنا که لازم است.
                    </p>
                </div>
            </div>
            <div class="column">
                <div class="box width-550px has-background-grey-lighter is-hidden-mobile">
                    <div class="is-flex is-align-items-center">
                        <p class=" has-text-grey">
                            ناشناس
                        </p>
                        <span class="dot-small mr-2 has-background-grey"></span>
                        <p class="mr-2 has-text-grey">
                            2 روز پیش
                        </p>
                    </div>
                    <p class="my-2 has-text-black">
                        خوب هست پیشنهاد میکنم!
                    </p>
                    <p class="has-text-justified">
                        لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است
                        چاپگرها و متون بلکه روزنامه و مجله در ستون و سطر آنچنا که لازم است.
                    </p>
                    <div class="has-text-left">
                        <img src="Like.png" alt="" class="mr-4">
                        <img src="Dislike.png" alt="" class="mr-3">
                    </div>
                </div>
                <div class="box has-background-grey-lighter is-hidden-desktop">
                    <div class="is-flex is-align-items-center">
                        <p class=" has-text-grey">
                            ناشناس
                        </p>
                        <span class="dot-small mr-2 has-background-grey"></span>
                        <p class="mr-2 has-text-grey">
                            2 روز پیش
                        </p>
                    </div>
                    <p class="my-2 has-text-black">
                        خوب هست پیشنهاد میکنم!
                    </p>
                    <p class="has-text-justified">
                        لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است
                        چاپگرها و متون بلکه روزنامه و مجله در ستون و سطر آنچنا که لازم است.
                    </p>
                </div>
            </div>
        </div>
        <div class="is-flex is-justify-content-left is-align-items-center is-hidden-desktop is-hidden-tablet">
            <button class="button is-black has-text-white">
                افزودن نظر +
            </button>
            <p class="mx-5">
                دو دیدگاه
            </p>
        </div>
        <p class="is-size-4 has-text-black mt-6 font-bold-number mr-6">
            محصولات مشابه
        </p>
        <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
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
    </div>
</template>
<script>
export default {
    data() {
        return {
            images: [
                { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false },
                { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false },
                { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false },
                { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false }
            ],
            number: 1,
            falseshow: true,
            currentSlide: 0,
            slides: [
                { image: 'siman450.png', alt: ' سیمان 50 کیلویی', },
                { image: 'siman450.png', alt: ' سیمان 50 کیلویی', },
            ],
        }
    },
    methods: {
        changeSlide(index) {
            this.currentSlide = index;
        },
        prevSlide() {
            this.currentSlide = (this.currentSlide - 1 + this.slides.length) % this.slides.length;
        },
        nextSlide() {
            this.currentSlide = (this.currentSlide + 1) % this.slides.length;
        },
        activebutton() {
            this.falseshow = !this.falseshow;
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
        },
        incrementnumber() {
            this.number++;
        },
        decrementnumber() {
            this.number--;
        }
    }
}
</script>
<style>
.background-black-input {
    border: 1px solid #5B5B5B;

}

.width-432px {
    width: 100%;
    background-color: #9D9D9D47;
}

.three-dots {
    height: 10px;
    width: 10px;
    border-radius: 50%;
    display: inline-block;
}

.background-black {
    background-color: #171717;
}

.border-grey {
    border: 1px solid #B5B5B5;
}

.test {
    border-radius: 5px;
    width: 37px;
    height: 37px;
    box-shadow: 0px 0px 0px 5px white;
    top: -20px;
}

.test img {
    width: 20px;
    height: 20px;
}

.width-550px {
    width: 550px;
    height: auto;
}

.img-background-black {
    background-image: url('/backgroundcolumn.png');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

.color-red {
    color: red;
}

.back-color-F8F8F8 {
    border: 2px solid #b7b7b7;
    background-color: #F8F8F8;
}

.white-hr {
    width: 63px;
    position: absolute;
    top: -1195%;
    right: 0;
}

.dot-small {
    height: 5px;
    width: 5px;
    border-radius: 50%;
    display: inline-block;
}
</style>
