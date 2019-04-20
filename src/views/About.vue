<template>
  <div class="about">
    <div class="history">
      <p class="display-2 font-weight-black">経歴</p>
      <v-card flat app>
        <v-card-text
          style="white-space: pre-line"
          class="blue-grey lighten-5"
        >{{ card_text_hisroty }}</v-card-text>
      </v-card>
    </div>
    <div class="hobby">
      <p class="display-2 font-weight-black">スキル</p>
      <v-card flat app>
        <v-card-text style="white-space: pre-wrap" class="blue-grey lighten-5">{{ card_text_skil }}</v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      card_text_hisroty: `1996年 - 愛媛県
      2015年 - 島根大学総合理工学部数理・情報システム学科 入学
      2019年 - 島根大学総合理工学部数理・情報システム学科 卒業
      2019年 - 奈良先端科学技術大学院大学先端科学研究科 入学
      `,
      card_text_skil: `Python      Ruby      機械学習      少しだけ(HTML      CSS      JavaScript      Vue.js)      
      `
    };
  }
};
</script>

<style>
.about {
  margin: 0 auto;
  margin-top: 30px;
  max-width: 767px;
}
</style>
