<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">Кормление и режим</h2>
          <div class="screen__content">
            <div class="screen__info">
              <p class="screen__text">Основой рациона голубей являются зерно и сочная зелень. <br />В рационе должны присутствовать:</p>
              <ul class="screen__text">
                <li>просо – 10%;</li>
                <li>пшеница – 30%;</li>
                <li>ячмень – 50%;</li>
                <li>остальные зерновые и семена (чечевица, семечки подсолнуха, овёс, горох) – 10%.</li>
              </ul>
              <p class="screen__text">В качестве зелени - шпинат, щавель, люцерна, крапива, клевер, салат, капуста.</p>
              <h2 class="screen__subtitle" style="margin-top: 60px">ПИТАНИЕ</h2>
              <h2 class="screen__subtitle screen__subtitle_h3">Лето</h2>
              <p class="screen__text">Кормление дважды в день: в 6-7 часов утра и в 6 часов вечера.</p>
              <h2 class="screen__subtitle screen__subtitle_h3">Зима</h2>
              <p class="screen__text">Кормление трижды в день: в 9 часов утра, в 2 часа дня, в 8 часов вечера.</p>
              <p class="screen__text">В период выкармливания птенцов - трёхразовое питание: в 5 часов утра, в час дня, в 9 часов вечера.</p>
              <p class="screen__text">Допускаются минеральные добавки: дроблёная ракушка, скорлупа яиц в измельчённом виде, соль, древесный уголь.</p>
              <p class="screen__text">
                Объем порций для птиц зависит от возраста и особенностей жизненного периода, в среднем это от 30 г до 60 г корма. Когда голубей готовят к
                соревнованиям, тратится много энергии. В это время необходимо ввести в рацион крахмал (давать птицам рис) и сахар.
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
  name: "Page-13",
  data() {
    return {
      pagePrev: 'page-12',
      pageNext: 'page-14',
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