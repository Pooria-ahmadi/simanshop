<template>
  <div class="is-hidden-tablet-only is-hidden-mobile ">
    <div class="box py-0">
      <div class="columns max-width-1160px is-vcentered">
        <div class="column">
          <div class="navbar-start is-hidden-mobile ">
            <NuxtLink class="navbar-item has-text-grey" to="/">
              خانه
            </NuxtLink>
            <div class="navbar-item has-dropdown is-hoverable">
              <NuxtLink class="navbar-item has-text-grey" to="/">
              محصولات
            </NuxtLink>

              <div class="navbar-dropdown">
                <div class="navbar-item is-justify-content-center is-underlined my-5">
                  دسته بندی
                </div>
                <a class="navbar-item mb-4">
                  سیمان
                </a>
                <a class="navbar-item mb-4">
                  گچ
                </a>
                <a class="navbar-item mb-4">
                 ماسه
                </a>
                <a class="navbar-item mb-4">
                 بتن
                </a>
                <a class="navbar-item mb-4">
                 سیمان سفید
                </a>
                <a class="navbar-item mb-4">
                 سیمان سفید
                </a>
              </div>
            </div>
            <NuxtLink class="navbar-item has-text-grey" to="/">
              درباره ما
            </NuxtLink>
            <NuxtLink class="navbar-item has-text-grey" to="/">
              ثبت نام/ ورود
            </NuxtLink>
          </div>
        </div>
        <div class="column">
          <div class="navbar-end is-hidden-mobile">
            <NuxtLink class="has-text-black" to="/">
              سیمان شاپ
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
a::before {
  content: '';
  display: block;
  position: absolute;
  bottom: 3px;
  left: 0;
  height: 2px;
  width: 100%;
  background-color: #585858;
  transform-origin: left;
  transform: scale(0, 1);
  transition: color 0.1s, transform 0.2s ease-out;
}

a:hover::before,
a:focus::before {
  transform-origin: right;
  transform: scale(1, 1);

}
</style>