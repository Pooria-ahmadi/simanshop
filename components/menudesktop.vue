<template>
  <div class="is-hidden-tablet-only">
    <div class="box is-hidden-mobile py-0">
      <div class="columns max-width-1160px is-vcentered">
        <div class="column">
          <div class="navbar-start is-hidden-mobile ">
            <NuxtLink class="navbar-item has-text-grey" to="/">
              خانه
            </NuxtLink> 
            <NuxtLink class="navbar-item has-text-grey" to="/shivar">
              محصولات
            </NuxtLink>
            <NuxtLink class="navbar-item has-text-grey" to="/shahi">
              درباره ما
            </NuxtLink>
            <NuxtLink class="navbar-item has-text-grey" to="/shahi">
              ورود / ثبت نام
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