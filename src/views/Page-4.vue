<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">Бой иранских голубей</h2>
          <div style="transform: translateY(-30px)" class="screen__content">
            <div class="screen__images">
              <div style="width: 800px; height: 425px" class="screen__image screen__image-ibg">
                <img src="img/1.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <p class="screen__text">
                «Иранцы» - бойная порода. Это означает, что при полёте птицы издают характерные щелчки. Бой крыльями хорошо различим даже с огромной высоты
                и делится на три категории.
              </p>
              <ul class="screen__text">
                <li>
                  Штопорный. Птица поднимается в высоту вертикально, кружится, совершая спиральные движения, непрерывно играет, показывая свои умения.
                  Такой подъём требует от голубя силы и является утомительным. Поэтому тренировать таким боем птицу следует не чаще двух раз в неделю.
                </li>
                <li>
                  Столбовой. Птица способна мгновенно набрать высоту, взлетать вертикально и совершать краткие круговые полёты. При этом во время взмаха
                  крыльев слышны своеобразные щелчки. После набора высоты птицы кувыркаются через голову. Завершающий этап – принятие исходного положения,
                  снижение плавными кругами.
                </li>
                <li>Игра бабочкой. Выполняется птицей в одиночном полете и сопровождается частым боем.</li>
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
import Doves from "@/components/Doves";
import Logo from "@/components/Logo";
import Background from "@/components/Background";

export default {
  name: "Page-4",
  data() {
    return {
      pagePrev: 'page-3',
      pageNext: 'page-5',
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