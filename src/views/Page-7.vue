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
                <img src="img/4.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <h2 class="screen__subtitle screen__subtitle_h3">Тегеранские высоколётные</h2>
              <p class="screen__text">
                Тегеранские голуби являются популярным и известным видом. Эти птицы отличаются разнообразием оттенков и узоров.Их легко распознать по
                коротковатому клюву и округлой голове. Пернатые очень похожи на ястреба. Эти птицы обладают внушительным размахом крыльев – он может
                достигать 70 см.
              </p>
              <p class="screen__text">
                Визитной карточкой тегеранских голубей являются цветные глаза - чем они ярче, тем больше ценятся в Иране. Оттенки могут быть от
                бледно-жёлтого до насыщенного красного. В приоритете глаза цвета апельсиновой корки. У чистокровной пакистанской птицы чаще всего
                встречается голубые и серые глаза.
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
  name: "Page-7",
  data() {
    return {
      pagePrev: 'page-6',
      pageNext: 'page-8',
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