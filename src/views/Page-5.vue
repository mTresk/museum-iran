<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">Разновидности</h2>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 800px; height: 530px" class="screen__image screen__image-ibg">
                <img src="img/2.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <h2 class="screen__subtitle screen__subtitle_h3">Тебризские голуби</h2>
              <p class="screen__text">
                Порода встречается в городе Тебриз и называют её Пар-Парли (Par-Parlee). Отличительная особенность - цвет (он может быть любым) и
                оперённость ног (чем длиннее перья на ногах, тем лучше). Птица в большинстве своём гладкоголовая. У особей вытянутая голова и удлиненный
                корпус. Порода обладает неплохими лётными качествами и частой игрой.
              </p>
              <p class="screen__text">
                Является самым распространенным видом на западных землях Ирана. Прямыми родственниками этих голубей считают бакинских летунов. Жители Ирана
                отмечают, что невозможно полностью узнать, как была выведена эта разновидность. Даже самый опытный голубевод всегда может узнать о древней
                птице что-то новое.
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
  name: "Page-5",
  data() {
    return {
      pagePrev: 'page-4',
      pageNext: 'page-6',
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