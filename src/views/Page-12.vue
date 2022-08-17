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
                <img src="img/9.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <h2 class="screen__subtitle screen__subtitle_h3">Гнезда</h2>
              <p class="screen__text">
                Оптимальный размер гнезда – 80х40х30 см. Самки иранской породы предпочитают самостоятельно обустраивать гнёзда. Птицеводу в такой ситуации
                понадобится лишь снабдить голубей строительным материалом: соломой, ветками, сеном.
              </p>
              <h2 class="screen__subtitle screen__subtitle_h3">Вентиляция</h2>
              <p class="screen__text">
                Система вентиляции поможет проветривать помещение, избавляя его от неприятных запахов, углекислого газа от помета. В птичнике всегда будет
                свежо. Лучше всего соорудить за основной дверью решётчатую. Также не помешают небольшие сетчатые отверстия на полу. На потолке необходимо
                смонтировать закрывающуюся трубу для вытяжки.
              </p>
              <h2 class="screen__subtitle screen__subtitle_h3">Дворик для выгула</h2>
              <p class="screen__text">
                По размерам он должен быть не меньше, чем голубятня. Сверху и со всех сторон территорию ограждают металлической сеткой, на пол стелют доску
                или кладут фанеру.
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
  name: "Page-12",
  data() {
    return {
      pagePrev: 'page-11',
      pageNext: 'page-13',
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