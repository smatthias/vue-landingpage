<script setup>
import { themeColor } from "../data/items";
//import { GeneralSearch } from "./helpers/GeneralSearch.vue"

const ZuruMainHeading = "Discover Kenya, Your Way — With Zuru, the Spirit of Adventure";
const buttonSeeFeature = "See Features";
const buttonPricing = "Pricing";
</script>

<template>
  <div class="untree_co-hero" id="home-section">
    <div class="container with-background">
      <div class="row align-items-center">
        <div class="row align-items-center">
          <div
            class="col-lg-7 ml-auto order-lg-2"
            data-aos="fade-right"
            data-aos-delay="400"
          >
          </div>

          <div class="col-lg-5">
            <h1 class="heading" data-aos="fade-up" data-aos-delay="0">
              {{ ZuruMainHeading }}
            </h1>
            <div class="excerpt" data-aos="fade-up" data-aos-delay="100">
              <p>
                Another cool free html css template by
                <span
                  style="
                    background-color: rgba(64, 123, 255, 0.07);
                    color: #407bff;
                  "
                  >Colorlib</span
                >
                Far far away, behind the word mountains, far from the
                countries Vokalia and Consonantia, there live the blind texts.
                Separated they live in Bookmarksgrove right at the coast
              </p>
            </div>
            <p data-aos="fade-up" data-aos-delay="200">
              <a
                href="#features-section"
                class="btn btn-primary smoothscroll"
                style="margin-right: 5px"
                :style="[
                  { background: themeColor },
                  { borderColor: themeColor },
                ]"
                >{{ buttonSeeFeature }}</a
              >
              <a
                href="#pricing-section"
                class="btn btn-outline-primary smoothscroll pricing"
                :style="[{ color: themeColor }, { borderColor: themeColor }]"
                >{{ buttonPricing }}</a
              >
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.pricing:hover {
  color: #fff !important;
}
</style>
