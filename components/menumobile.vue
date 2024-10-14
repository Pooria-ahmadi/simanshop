<template>
    <div class="is-hidden-desktop">
        <div class="columns mx-0 py-0 is-mobile box is-hidden-desktop is-vcentered">
            <div class="column pb-0">
                <div class="navbar-burger" @click="toggleMenu">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>
            <div class="column pb-0 has-text-left">
                <p>
                    سیمان شاپ
                </p>
            </div>
        </div>
        <div class="navbar-menu pr-6 is-hidden-desktop" :class="{ 'is-active': isMobileMenuOpen }">
            <ul>
                <li class="my-4">
                    <NuxtLink class="has-text-black has-text-weight-semibold" to="/">
                        خانه
                    </NuxtLink>
                </li>
                <li class="my-4">
                    <NuxtLink class="has-text-black has-text-weight-semibold" to="/">
                        محصولات
                    </NuxtLink>
                </li>
                <li class="my-4">
                    <NuxtLink class="has-text-black has-text-weight-semibold" to="/">
                        درباره ما
                    </NuxtLink>
                </li>
                <li class="my-4">
                    <NuxtLink class="has-text-black has-text-weight-semibold" to="/">
                        ورود / ثبت نام
                    </NuxtLink>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            isMobileMenuOpen: false,
        };
    },
    methods: {
        toggleMenu() {
            this.isMobileMenuOpen = !this.isMobileMenuOpen;
        }
    },
}
</script>
<style>
.cart-icon {
    position: relative;
    display: inline-block;
}

.cart-count {
    position: absolute;
    top: -10px;
    right: -10px;
    background-color: rgb(1, 252, 22);
    color: white;
    border-radius: 50%;
    padding: 5px 10px;
    font-size: 12px;
}
</style>