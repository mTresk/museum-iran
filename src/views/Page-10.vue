<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">Голубятня. Условия содержания</h2>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 800px; height: 530px" class="screen__image screen__image-ibg">
                <img src="img/7.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <h2 class="screen__subtitle screen__subtitle_h3">Местоположение</h2>
              <p class="screen__text">
                Иранские голуби обладают плохим здоровьем, поэтому важно размещать голубятню вдали от источников инфекции: выгребных ям, фермерских угодий,
                свинарников, птичников и т. д.
              </p>
              <p class="screen__text">Желательно строить здание там, где рядом отсутствуют электрические линии и высокие деревья.</p>
              <h2 class="screen__subtitle screen__subtitle_h3">Габариты голубятни, плотность посадки</h2>
              <p class="screen__text">
                Высота голубятни может достигать 2 м. На одну пару птиц приходится не менее 50 куб. см. К этому пространству требуется добавить место для
                гнёзд, кормушек и поилок.
              </p>
              <h2 class="screen__subtitle screen__subtitle_h3">Утепление</h2>
              <p class="screen__text">
                Желательно утеплить и герметизировать птичник. В помещении не должно быть щелей. Обязательно наличие подстилки, её меняют регулярно – это
                позволяет избежать появления сырости. Оптимальная температура в летний период составляет +20 градусов, в зимнее время – 5-7 градусов тепла.
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
  name: "Page-10",
  data() {
    return {
      pagePrev: 'page-9',
      pageNext: 'page-11',
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