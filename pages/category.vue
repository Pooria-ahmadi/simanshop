<template>
    <div class="is-relative">
        <div class="max-width-1160px mt-6 py-6">
            <p class="mt-5 is-size-4 has-text-black">
                محصولات : گچ
            </p>
            <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
                <div class="column has-text-centered is-one-quarter is-three-fifths-mobile"
                    v-for="(image, index) in images" :key="index">

                    <div class="image-container">
                        <NuxtLink to="/product">
                            <img :src="image.src" :alt="image.alt">
                        </NuxtLink>
                        <div v-if="image.showlike" class="corner-like has-background-black p-2"
                            @click="activelike(index)">
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


            <p class="mt-5 is-size-4 has-text-black">
                محصولات : سیمان
            </p>
            <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
                <div class="column has-text-centered is-one-quarter is-three-fifths-mobile"
                    v-for="(image, index) in images" :key="index">

                    <div class="image-container">
                        <NuxtLink to="/product">
                            <img :src="image.src" :alt="image.alt">
                        </NuxtLink>
                        <div v-if="image.showlike" class="corner-like has-background-black p-2"
                            @click="activelike(index)">
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

            <p class="mt-5 is-size-4 has-text-black">
                محصولات : بتن
            </p>
            <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
                <div class="column has-text-centered is-one-quarter is-three-fifths-mobile"
                    v-for="(image, index) in images" :key="index">

                    <div class="image-container">
                        <NuxtLink to="/product">
                            <img :src="image.src" :alt="image.alt">
                        </NuxtLink>
                        <div v-if="image.showlike" class="corner-like has-background-black p-2"
                            @click="activelike(index)">
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
            <p class="mt-5 is-size-4 has-text-black">
                محصولات : ملات
            </p>
            <div class="columns mx-0 mt-5 is-flex-mobile overflow-x-auto">
                <div class="column has-text-centered is-one-quarter is-three-fifths-mobile"
                    v-for="(image, index) in images" :key="index">

                    <div class="image-container">
                        <NuxtLink to="/product">
                            <img :src="image.src" :alt="image.alt">
                        </NuxtLink>
                        <div v-if="image.showlike" class="corner-like has-background-black p-2"
                            @click="activelike(index)">
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
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            images: [
                { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false, showlike: true },
                { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false, showlike: true },
                { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false, showlike: true },
                { src: 'siman4.png', caption: 'سیمان 50 کیلویی', price: '115,000', alt: 'سیمان 50 کیلویی', number: 0, showCart: false, showlike: true }
            ],

        }
    },
    methods: {
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

