<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 800px; height: 600px" class="screen__image screen__image-ibg">
                <img src="img/6.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <h2 class="screen__subtitle screen__subtitle_h3">Щекатые (карагезы)</h2>
              <p class="screen__text">
                Щекатые голуби сочетают в себе помесь тебризских и тегеранских птиц. У «иранцев» имеется своеобразный рисунок на оперении, что делает
                разновидность узнаваемой среди остальных пород. Основным цветом перьев является белый оттенок, но щёки и голова могут быть красного или
                жёлтого цвета. У щекатых «иранцев» стройный корпус и гладкая голова.
              </p>
            </div>
          </div>
          <Navigation :page-next="pageNext" :page-prev="pagePrev"/>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import {mapActions} from 'vuex'
import Navigation from "@/components/Navigation";
import Doves from "@/components/Doves";
import Logo from "@/components/Logo";
import Background from "@/components/Background";

export default {
  name: "Page-9",
  data() {
    return {
      pagePrev: 'page-8',
      pageNext: 'page-10',
    }
  },
  components: {
    Doves,
    Logo,
    Background,
    Navigation
  },
  mounted() {
    this.animate()
  },
  methods: {
    ...mapActions([
      'animate'
    ]),
  }
}
</script>