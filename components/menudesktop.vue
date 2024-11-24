<template>
  <div class="fixed">
    <div class="box py-0 mb-3">
      <div class="columns max-width-1160px is-vcentered py-1 mb-2">
        <div class="column py-0 is-flex is-justify-content-right">
          <nav class="navbar">
            <div class="navbar-brand">
              <button class="navbar-burger" :class="{ 'is-active': isMenuActive }" aria-label="menu"
                aria-expanded="false" @click="toggleMenu">
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
              </button>
            </div>

            <div  class="navbar-menu" :class="{ 'is-active': isMenuActive }" style="box-shadow: none;">
              <div class="navbar-start">
                <NuxtLink class="navbar-item has-text-grey text-hover-black" to="/">
                  خانه
                </NuxtLink>
                <div class="navbar-item has-dropdown is-hoverable ">
                  <NuxtLink class="navbar-item has-text-grey text-hover-black bg-transparent" to="/category">
                    محصولات
                  </NuxtLink>
                  <div class="navbar-dropdown">
                    <NuxtLink class="navbar-item" to="/category">
                      <p class="has-text-black">دسته بندی</p>
                    </NuxtLink>
                    <hr class="navbar-divider">
                    <ul>
                      <li class="has-subcategory">
                        <NuxtLink class="navbar-item text-hover-black" to="/">سیمان</NuxtLink>
                        <div class="subcategory-box has-background-white p-4">
                          <p class="has-text-info">
                            همه محصولات سیمان >
                          </p>
                          <p class="has-text-black has-text-centered is-underlined is-size-6 my-4"> انواع سیمان</p>
                          <ul>
                            <li class="subcategory-item width-178px" v-for="(siman, index) in menusiman" :key="index">{{ siman }}</li>
                          </ul>
                        </div>
                      </li>
                      <li>
                        <NuxtLink class="navbar-item" to="#" v-for="(menu, index) in menuforShopData" :key="index">
                          {{ menu }}</NuxtLink>
                      </li>
                    </ul>
                  </div>
                </div>
                <NuxtLink class="navbar-item has-text-grey text-hover-black" to="/aboutus">
                  درباره ما
                </NuxtLink>
                <NuxtLink class="navbar-item has-text-grey text-hover-black" to="/login">
                  ثبت نام/ ورود
                </NuxtLink>
              </div>
            </div>
          </nav>
        </div>
        <div class="column py-0 is-flex is-align-items-center is-justify-content-end">
          <NuxtLink to="/" class="is-flex is-align-items-center">
            <img src="logo.jpg" alt="لوگوی سیمان شاپ" class="logo-img">
            <span class="has-text-black ml-2">سیمان شاپ</span>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenuActive: false,
      menuforShopData: [],
      menusiman:[],
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuActive = !this.isMenuActive;
    },
    fetchMenuData() {
      this.$axios
        .get("https://fapi.simanshop.com/api/auth/MenusForShop")
        .then((response) => {
          this.menuforShopData = response.data
            .slice(0, 6)
            .filter((_, index) => index !== 2)
            .map((item) => item.menuforshop);
        })
    },
    fetchsimanData() {
      this.$axios
        .get("https://fapi.simanshop.com/api/auth/MenusForShop")
        .then((response) => {
          this.menusiman = response.data
            .slice(6, 10)
            .map((item) => item.menuforshop);
        })
    },
  },
  mounted() {
    this.fetchMenuData();
    this.fetchsimanData();
  },
}
</script>

<style scoped>
.width-178px{
  width: 178px;
}
.has-subcategory {
  position: relative;
}

.bg-hover-none {
  background-color: transparent;
}

.subcategory-box {
  position: absolute;
  top: -58px;
  right: 100%;
  width: 200px;
  display: none;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  
}

.has-subcategory:hover .subcategory-box {
  display: block;
}

.has-subcategory:hover .subcategory-box {
  display: block;
}

.subcategory-item {
  padding: 10px;
  cursor: pointer;
  text-align: center;
  font-size: 14px;
  color: #333;
}

.subcategory-item:hover {
  background-color: #f4f4f4;
  color: #000;
}

.text-hover-black:hover {
  color: black;
}
.bg-transparent {
  background-color: transparent; /* پس‌زمینه شفاف */
  transition: color 0.3s ease, background-color 0.3s ease; /* برای ایجاد انیمیشن */
}

.bg-transparent:hover {
  color: black;
}
</style>
