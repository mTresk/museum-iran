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
                <img src="img/8.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <h2 class="screen__subtitle screen__subtitle_h3">Подстилка</h2>
              <p class="screen__text">
                Обязательное условие в зимнее время года. Подстилку изготавливают из сена и соломы, опилок, небольших веток, песка или сухого торфа. Толщина
                подстилки составляет около 5-10 см. Под неё насыпают древесную золу или полынь – они помогают предотвратить заражение инфекционными
                заболеваниями.
              </p>
              <h2 class="screen__subtitle screen__subtitle_h3">Кормушки и поилки</h2>
              <p class="screen__text">
                Опытные голубеводы рекомендуют устанавливать автоматические кормушки, ведь это позволяет минимизировать участие человека в уходе за
                голубями.
              </p>
              <h2 class="screen__subtitle screen__subtitle_h3">Насесты</h2>
              <p class="screen__text">
                От численности голубей зависит количество насестов. Обычно их выполняют из деревянных брусьев, перпендикулярно закрепляя на стене.
                Расстояние от пола до потолка составляет более 50 см.
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
  name: "Page-11",
  data() {
    return {
      pagePrev: 'page-10',
      pageNext: 'page-12',
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