<template>
  <div class="is-hidden-tablet-only is-hidden-mobile fixed">
    <div class="box py-0 mb-3">
      <div class="columns max-width-1160px is-vcentered py-1 mb-2">
        <div class="column">
          <div class="is-flex">
            <NuxtLink class="has-text-grey text-hover-black" to="/">
              خانه
            </NuxtLink>
            <div class="is-relative has-dropdown">
              <NuxtLink class="has-text-grey text-hover-black pr-5 pb-5" to="/category">
                محصولات
              </NuxtLink>
              <div class="category-box has-background-white p-5">
                <NuxtLink to="/category">
                  <p class="has-text-black">دسته بندی</p>
                </NuxtLink>
                <hr class="mt-2 width-70px">
                <ul>
                  <div class="has-subcategory" style="width: 181px;">
                    <div style="width: 150px;">
                      <li class="pr-3 category-item py-1 border-radius">سیمان</li>
                    </div>
                    <div class="subcategory-box has-background-white p-4">
                      <hr class="vl">
                      <a href="#" class="py-5">همه محصولات سیمان ></a>
                      <p class="has-text-black pt-5 mt-4">انواع سیمان</p>
                      <hr class="mt-2 width-70px">
                      <ul>
                        <li class="mt-4 pr-3 category-item py-1 border-radius has-submenu">
                          سیمان پرتلند
                          <ul class="sub-subcategory has-background-white px-4">
                            <hr class="vl-2">
                            <p class="has-text-black pt-5 mt-4">سیمان پرتلند </p>
                            <hr class="mt-2 width-70px">
                            <li class="mt-4 pr-3 category-item py-1 border-radius has-text-grey">سیمان پرتلند تیپ 1</li>
                            <li class="mt-4 pr-3 category-item py-1 border-radius has-text-grey">سیمان پرتلند تیپ 2</li>
                            <li class="mt-4 pr-3 category-item py-1 border-radius has-text-grey">سیمان پرتلند تیپ 3</li>
                            <li class="mt-4 pr-3 category-item py-1 border-radius has-text-grey">سیمان پرتلند تیپ 4</li>
                          </ul>
                        </li>
                        <li class="mt-4 pr-3 category-item py-1 border-radius">سیمان رنگی</li>
                        <li class="mt-4 pr-3 category-item py-1 border-radius">سیمان نسوز</li>
                      </ul>
                    </div>
                  </div>
                  <li class="mt-4 pr-3 category-item py-1 border-radius">گچ</li>
                  <li class="mt-4 pr-3 category-item py-1 border-radius">ماسه</li>
                  <li class="mt-4 pr-3 category-item py-1 border-radius">بتن</li>
                  <li class="mt-4 pr-3 category-item py-1 border-radius">سیمان سفید</li>
                  <li class="mt-4 pr-3 category-item py-1 border-radius">پودر سنگ</li>
                  <li class="mt-4 pr-3 category-item py-1 border-radius">ملات</li>
                </ul>
              </div>
            </div>

            <NuxtLink class="has-text-grey text-hover-black pr-5" to="/aboutus">
              درباره ما
            </NuxtLink>
            <NuxtLink class="has-text-grey text-hover-black pr-5" to="/login">
              ثبت نام/ ورود
            </NuxtLink>
          </div>
        </div>
        <div class="column">
          <div class="navbar-end is-hidden-mobile">
            <NuxtLink class="has-text-black is-align-content-center" to="/">
              سیمان شاپ
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style>
.category-box {
  position: absolute;
  top: 48px;
  right: 20px;
  width: 200px;
  display: none;

}

.has-dropdown:hover .category-box {
  display: block;
}

.has-subcategory {
  position: relative;
}

.subcategory-box {
  display: none;
  position: absolute;
  top: -82px;
  right: 97%;
  width: 200px;
  height: 426px;
}

.has-subcategory:hover .subcategory-box {
  display: block;
}

.has-submenu {
  position: relative;
}

.sub-subcategory {
  display: none;
  position: absolute;
  top: -139px;
  left: -200px;
  width: 200px;
  height: 426px;
  padding-top: 40px;
}

.has-submenu:hover .sub-subcategory {
  display: block;
}

.width-70px {
  width: 70px;
  background-color: black;
}

.category-item {
  cursor: pointer;
}

.category-item:hover {
  background-color: #d4d4d4;
  color: black;
}

.text-hover-black:hover {
  color: black !important;
}

.vl {
  border-left: 1px solid #a6a6a6;
  height: 374px;
  position: absolute;
  right: 43%;
  margin-right: -86px;
  top: 23px;
}
.vl-2{
  border-left: 1px solid #a6a6a6;
  height: 304px;
  position: absolute;
  right: 45%;
  margin-right: -86px;
  top: 90px;
}
</style>
