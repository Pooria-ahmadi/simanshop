<template>
    <div style="overflow: hidden;">
        <div class="max-width-1160px " style="margin-top: 80px;">
            <div class="columns is-centered mx-0 is-vcentered">
                <div class="column is-half has-background-white mx-auto py-0 my-0">
                    <div class="columns is-centered">
                        <div class="column box is-8-desktop is-10-mobile mx-auto border-radius-search-input-header">
                            <p class="is-size-4 has-text-black my-4">
                                ورود | ثبت نام
                            </p>
                            <p class="has-text-black is-size-6">جهت ورود شماره موبایل خود را وارد کنید</p>
                            <div class="control mt-6">
                                <label class="label has-text-black "> شماره موبایل </label>
                                <input class="input border-radius" type="text" placeholder="*شماره موبایل" />
                            </div>
                            <button class="button is-black width-100 border-radius mt-6 mb-5">ارسال</button>
                        </div>
                    </div>
                </div>
                <div class="column has-text-centered p-0 is-hidden-mobile">
                    <img src="login.jpg" alt="صفحه ورود سیمان شاپ" style="height: 570px;">
                </div>
            </div>
        </div>
    </div>
</template>
<style>
.width-100{
    width: 100%;
}
</style>
<script>
export default {
    layout: 'login'
}
</script>
