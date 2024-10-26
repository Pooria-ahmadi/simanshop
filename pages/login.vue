<template>
    <div class="max-width-1160px ">
        <div class="columns mx-0 is-centered m-0 p-0 ">
            <div class="column is-10 p-0 m-0 ">
                <div class="image-background-cover ">
                    <img src="siman10.jpg" alt="صفحه لاگین" class="image-background-cover-img">
                    <div class="box custom-box border-radius is-align-content-center">
                        <div class="has-text-centered">
                            <NuxtLink to="/">
                                <img src="logo2.png" alt="لوگو">
                            </NuxtLink>
                        </div>
                        <div class="has-text-centered my-4">
                            <NuxtLink to="/" class="has-text-warning">
                            جهت ورود به سایت >
                        </NuxtLink>
                        </div> 
                        <label class="label has-text-white py-3">جهت خرید شماره موبایل خود را وارد نمائید</label>
                        <div class="control">
                            <input class="input is-rounded" type="text" placeholder="شماره موبایل خود را وارد کنید">
                        </div>
                        <div class="control mt-4 has-text-centered">
                            <button class="button is-primary is-rounded">ارسال</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    layout:'login'
}
</script>

<style>
.image-background-cover {
    position: relative;
}

.image-background-cover-img {
    width: 100%;
    border-radius: 0px 15px 15px 15px;
    height: 100vh;
    object-fit: cover;
}

.custom-box {
    background-color: rgba(17, 17, 17, 0.82);
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 375px;
}
</style>