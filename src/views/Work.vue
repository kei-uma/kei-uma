<template>
  <div class="work blue-grey lighten-5">
    <v-tabs
      slot="extension"
      v-model="model"
      centered
      color="blue-grey lighten-5"
      slider-color="black"
    >
      <v-tab v-for="i in items" :key="i.id" :href="`#tab-${i.id}`">{{ i.name }}</v-tab>
    </v-tabs>
    <div class="tab">
      <v-tabs-items v-model="model">
        <v-tab-item v-for="i in items" :key="i.id" :value="`tab-${i.id}`">
          <div class="summary">
            <p class="display-2 font-weight-black">概要</p>
            <v-card flat app>
              <v-card-text
                style="white-space: pre-line"
                class="blue-grey lighten-5"
              >{{ i.card_text }}</v-card-text>
            </v-card>
          </div>
          <div class="language">
            <p class="display-2 font-weight-black">使用言語と技術</p>
            <v-card flat app>
              <v-card-text
                style="white-space: pre-wrap"
                class="blue-grey lighten-5"
              >{{ i.languages }}</v-card-text>
            </v-card>
          </div>
          <div class="img">
            <div v-for="item in i.imagepath" :key="item">
              <v-img v-bind:src="item" class="image-size" max-width="300px" height="auto"/>
            </div>
          </div>
        </v-tab-item>
      </v-tabs-items>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      model: "tab-2",
      text:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      items: [
        {
          id: 1,
          name: "行動認識システム",
          card_text: `複数の非接触センサを活用して宅内の行動認識システムを構築しました。
            Raspberry pi zeroで複数の非接触センサのデータを取得し特徴量を抽出し機械学習を行いました。
            短時間フーリエ変換をセンサデータに適用し特徴量としています。
            機械学習ではRandom Forestにより学習モデルを構築しています。
            まだまだ認識精度が低く実用化に向けて研究中です。`,
          languages: `Python      Node.js      Fire Base      機械学習`
        },
        {
          id: 2,
          name: "Beeinfo",
          card_text: `本システムはTwitterのトレンドをまとめたキュレーションサイトです。
                      4人のチームで約1年間かけてアジャイル開発で企画、設計、構築まで行いました。
                      私は主にバックエンドの作業とフロントエンドの作業少しを担当しました。
                      Ruby on Railsでバックエンド側の処理を記述しています。
                      サーバはAWSを使用しました。(現在は稼働しておりません。)
                      半日に1回Twitterからトレンドとそれに関するツイートを取得しDBに格納します。
                      その後、管理者が気になるトレンドのツイートに関する記事をドラッグ&ドロップにより作成することができます。
                      ユーザは管理者が作成した記事を閲覧できます。ログイン機能を実装したことによりユーザの情報を記憶しています。
                      その他に、トップ画面のレイアウトをカスタマイズできる機能、記事のランキング機能、記事の検索等も実装しました。
                      `,
          languages: `Ruby on Rails      AWS      Mysql`,
          imagepath: [
            require("@/assets/beeinfotop.png"),
            require("@/assets/beeinfoarticle.png")
          ]
        },
        {
          id: 3,
          name: "Portfolio",
          card_text: `このサイトは自分についてや作ったものをまとめるために作成しました。
                      Vue.jsが最近人気であることと開発しやすそうとういことでVue.jsのVuetifyにより構築しています。
                      基本的にはVuetifyのフレームワークを利用し開発しています。
                      `,
          languages: `JavaScript      Vue.js      Vuetify`
        }
      ],
      overviews: [
        {
          id: 1
        }
      ]
    };
  }
};
</script>

<style>
.tab {
  margin: 0 auto;
  max-width: 767px;
}
.summary {
  list-style: none;
  margin-top: 30px;
}
.language {
  list-style: none;
}
.img {
  list-style: none;
}
.image-size {
  margin: 30px;
}
</style>
