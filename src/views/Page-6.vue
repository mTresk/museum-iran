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
                <img src="img/3.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <h2 class="screen__subtitle screen__subtitle_h3">Головатые</h2>
              <p class="screen__text">
                Отличительная черта – контрастный цвет оперения на голове. Пернатые характеризуются белоснежным оттенком перьев на теле, а оперение на
                голове и шее тёмного цвета варьируется от светло-коричневого до черного.
              </p>
              <p class="screen__text">
                Этот вид особенно ценится птицеводами потому что они с трудом идут на контакт с человеком, доставляют трудности в приручении, но при этом,
                достигнув результата, пернатые награждают голубевода красивым столбовым полётом.
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
  name: "Page-6",
  data() {
    return {
      pagePrev: 'page-5',
      pageNext: 'page-7',
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