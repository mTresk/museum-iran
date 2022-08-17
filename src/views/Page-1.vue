<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <div class="screen__content">
            <div class="screen__info">
              <h2 class="screen__subtitle">Иранские бойные голуби</h2>
              <p class="screen__text">
                Красивые, гармонично сложённые, горделивые птицы с завораживающей манерой полёта. В процессе подъёма на высоту голуби выполняют множество
                трюков. Летают стаями, но держатся поодиночке. Иранские голуби склонны летать медленно. В полёте, набирая высоту, птицы бьют крыльями по
                воздуху, создавая характерные звуки. Поэтому их и называют бойными. Именно это и является отличительной чертой и изюминкой породы.
              </p>
              <p class="screen__text">
                «Иранцы» – потомки персидских голубей, которых начали разводить более тысячи лет назад. Птиц тщательно отбирали, обращая внимание на такие
                критерии как красота, выносливость, высота полёта. Для определения лучших каждую весну проводились соревнования, в которых участвовало по 10
                птиц.
              </p>
              <p class="screen__text">
                Несмотря на продолжающиеся в этом регионе войны, местные жители продолжали любить голубей. Разводят птиц и теперь, сохраняя священную
                традицию. Фермами, где разводят иранских бойных голубей, владеют уважаемые люди.
              </p>
              <p class="screen__text">Отличительные характеристики иранских голубей:</p>
              <ul class="screen__text">
                <li>длинный и густотой хвост;</li>
                <li>более обтекаемая форма тела по сравнению с другими породами;</li>
                <li>чётко просматриваемый рельеф мускулов;</li>
                <li>высота полёта;</li>
                <li>использование различных приёмов во время полёта.</li>
              </ul>
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
import Background from "@/components/Background";
import Logo from "@/components/Logo";
import Doves from "@/components/Doves";

export default {
  name: "Page-1",
  data() {
    return {
      pageNext: 'page-2',
      pagePrev: 'home'
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