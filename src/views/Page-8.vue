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
                <img src="img/5.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <h2 class="screen__subtitle screen__subtitle_h3">Хамаданские бойные космачи</h2>
              <p class="screen__text">
                Местом выведения этой разновидности иранских голубей стала северо-западная часть иранских земель, а точнее, провинция Хамадан, благодаря
                чему птицы и получили свое название. У голубей длинные перья на ногах (до 20 см) – это украшение считается самым главным в их внешности.
              </p>
              <p class="screen__text">
                Хамаданские голубеводы из поколения в поколение передавали опыт по работе с косматыми голубями, в результате были сформированы целые линии,
                отличающиеся длинной клюва, рисунком оперения, и перьевым украшением головы. Популярны голуби с цветным рисунком на белом фоне тела
                (цветнобокие, цветнохвостые, зеркальные) и одноцветные (сизые, белые, жёлтые, красные).
              </p>
              <p class="screen__text">
                Хамаданские космачи - по лётным качествам не уступают голоногим породам, а бойные даже значительно превосходят. Хорошо натренированные
                голуби способны находится в воздухе 12-14 часов, то есть при утреннем гоне садятся они только поздно вечером.
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
  name: "Page-8",
  data() {
    return {
      pagePrev: 'page-7',
      pageNext: 'page-9',
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