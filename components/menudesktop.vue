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
            <div class="navbar-menu" :class="{ 'is-active': isMenuActive }" style="box-shadow: none;">
              <div class="navbar-start">
                <NuxtLink class="navbar-item has-text-grey text-hover-black" to="/">
                  خانه
                </NuxtLink>
                <div class="navbar-item has-dropdown is-hoverable">
                  <NuxtLink class="navbar-item has-text-grey text-hover-black bg-transparent" to="/category">
                    محصولات
                  </NuxtLink>
                  <div class="navbar-dropdown" style="border-top: none" >
                    <NuxtLink class="has-text-black is-underlined " to="/category">
                      <p class="has-text-black">دسته بندی</p>
                    </NuxtLink>
                    <hr class="navbar-divider">
                 
                      <ul>
                        <li v-for="(menu, index) in menuforShopData" :key="index" class="has-subcategory">
                          <div>
                            <NuxtLink class="navbar-item text-hover-black" to="#">
                              {{ menu }}
                            </NuxtLink>
                          </div>
                          <ul v-if="menusiman.length && index === 0" class="subcategory-box box px-0">
                            <li v-for="(submenu, subIndex) in menusiman" :key="subIndex" class="subcategory-item">
                              <NuxtLink class="has-text-black" to="#">
                                {{ submenu }}
                              </NuxtLink>
                            </li>
                          </ul>
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
          <NuxtLink to="/" class="is-flex is-align-items-center logo-mobile-up0">
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
      menusiman: [],

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
          const allData = response.data;
          this.menuforShopData = allData.slice(0, 6).map((item) => item.menuforshop);
          this.menusiman = allData.slice(6, 10).map((item) => item.menuforshop);
        })
    },
  },
  mounted() {
    this.fetchMenuData();
  },
}
</script>


<style scoped>
@media only screen and (max-width: 1023px) {
  .logo-mobile-up0 {
    position: absolute;
    left: 0;
    top: -3px;
    z-index: 10;
  }
}
.width-178px {
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
  background-color: transparent;
  transition: color 0.3s ease, background-color 0.3s ease;
}

.bg-transparent:hover {
  color: black;
}
</style>
