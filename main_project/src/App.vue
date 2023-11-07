<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <!-- nav -->
  <header class="header_sticky">
    <nav class="navbar navbar-expand-lg navbar-light bg-light nav_padding">
      <div class="container-fluid p-0 m-0">
        <a class="navbar-brand d-flex align-items-center" href="#">
          <img alt="logo" class="pe-2" src="@/assets/img/nav/logo.svg" width="52.17" height="43" />
          <h4 class="text-primary m-0">喵立翰 Miao Li-Han</h4>
        </a>
        <div class="text-secondary d-none d-lg-flex">
          <a class="nav-link px-3 active" aria-current="page" href="#section1">候選人主張</a>
          <a class="nav-link px-3" href="#section2">最新活動</a>
          <a class="nav-link px-3" href="#section3">政策議題</a>
          <a class="nav-link px-3" href="#section4">小額捐款</a>
          <a class="nav-link px-3" href="#section4">民眾服務信箱</a>
        </div>
        <div class="d-none d-sm-block">
          <a href="#" class="pe-3">
            <img src="@/assets/img/nav/fb_icon.svg " width="32" height="32" />
          </a>
          <a href="#" class="pe-3">
            <img src="@/assets/img/nav/ig_icon.svg " width="32" height="32" />
          </a>
          <a href="#">
            <img src="@/assets/img/nav/yt_icon.svg " width="32" height="32" />
          </a>
        </div>
      </div>
    </nav>

    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div> -->
  </header>
  <!-- 標題人物 -->
  <section>
    <div class="container big_title_margin">
      <div class="row">
        <div class="col-12 text-center pb-3">
          <p class="font_mantouSans big_title d-none d-lg-block">台灣的明天 喵先鋪路</p>
          <span class="font_mantouSans big_title d-lg-none">台灣的明天 </span>
          <br class="d-lg-none">
          <span class="font_mantouSans big_title d-lg-none">喵先鋪路</span>
        </div>
        <div class="col-12 text-center pb-3">
          <div class="row justify-content-center align-items-center">
            <div class="col-6 col-lg-2 img_container">
              <img class="mb-3 img_cover" src="@/assets/img/mainPage/2024_title.svg"/>
            </div>
            <div class="col-7 col-lg-3 img_container">
              <img class="mb-3 img_cover" src="@/assets/img/mainPage/name_title.svg"/>
            </div>
          </div>
        </div>
        <div class="col-12 text-center img_container">
          <img class="img_cover_70" src="@/assets/img/mainPage/man_and_bg.svg"/>
        </div>
      </div>
    </div>
    <div class="container-fluid m-0 p-0">
      <div class="row">
        <div class="col-12">
          <div class="marquee-container font_mantouSans marquee_title">
            <div class="marquee-content">
              為喵星人，護台灣！ 從喵的眼中，看見台灣 喵的未來，人的希望
            </div>
            <div class="marquee-content2">
              為喵星人，護台灣！ 從喵的眼中，看見台灣 喵的未來，人的希望
            </div>
            <div class="marquee-content3">
              為喵星人，護台灣！ 從喵的眼中，看見台灣 喵的未來，人的希望
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- 候選人主張 -->
  <section id="section1" class="text-secondary">
    <div class="container-fluid bg_advpcate">
      <div class="row container m-auto block_advpcate">
        <div class="col-12 content_bg">
          <div class="row justify-content-center align-items-center">
            <div class="col-lg-12 col-xl-6 advpcate_text_container">
              <div class="text-center">
                <img src="@/assets/img/advpcate/advpcate_tag.svg" width="114" height="35" />
              </div>
              <p class="font_mantouSans title text-center">候選人主張</p>
              <p class="sub_title">
                我堅信 ! 藉由推動更完善的<span class="text-primary">貓咪福利</span>和相關政策，
                更是間接地投資於<span class="text-primary">台灣的未來</span>。
              </p>
              <p>
                畢竟，民眾的身心健康與工作熱情是推動經濟的核心動力。透過完善的貓咪福利政策，為台灣的
                GDP 經濟帶來巨大效益。<br />
                因此，我期望能在立法院內推進這些政策，確保每一隻貓咪都能得到他們應有的照顧，同時也為台灣的經濟發展助一臂之力。讓我們一同護航台灣的幸福經濟，從照顧每一隻貓咪開始。
              </p>
            </div>
            <div class="col-lg-12 col-xl-6 advpcate_img_container">
              <div>
                <img class="img_cover" src="@/assets/img/advpcate/advpcate_man.svg" alt="" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!--最新活動 -->
  <!-- <section id="section2" class="text-secondary">
    <div class="row container block_last_events justify-content-center align-items-center">
      <div class="col-12">
        <div class="text-center">
          <img src="@/assets/img/lastEvents/last_event_tag.svg" alt="" width="154" height="35" />
        </div>
        <p class="font_mantouSans title text-center">最新活動</p>
      </div>
      <div class="col-6">
        <div class="row">
          <div class="col-12 img_container">
            <img src="@/assets/img/lastEvents/main_event.svg" alt="" />
          </div>
          <div class="col-12 mt-2">
            <p class="date_color">2023/12/26</p>
            <h5>參與台北寵物論壇，爭取貓咪友善環境</h5>
            <p>
              炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，
              決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中， 每一隻貓咪都應該有自己的 VIP
              休憩空間。
            </p>
          </div>
        </div>
      </div>
      <div class="col-6">
        <div class="row">
          <div class="col-12">
            <div class="row">
              <div class="col-4 event_content">
                <img src="@/assets/img/lastEvents/event_01.svg" alt="" />
              </div>
              <div class="col-8">
                <p class="date_color">2023/12/24</p>
                <h5>掃街模式開啟！帶著你的貓耳，來和我一起走！</h5>
                <p>
                  街上氣氛真的很棒，從小孩到大人，甚至有些狗狗朋友都帶著貓耳來找我握手，真的太可愛了！
                </p>
              </div>
            </div>
          </div>
          <div class="col-12">
            <div class="row">
              <div class="col-4 event_content">
                <img src="@/assets/img/lastEvents/event_02.svg" alt="" />
              </div>
              <div class="col-8">
                <p class="date_color">2023/12/20</p>
                <h5>收容所模特兒大比拼！</h5>
                <p>
                  今天的收容所不再是一片寂靜。為了讓更多人認識到這裡的毛孩子，我們舉辦了一場前所未有的「模特兒走秀」！
                </p>
              </div>
            </div>
          </div>
          <div class="col-12">
            <div class="row">
              <div class="col-4 event_content">
                <img src="@/assets/img/lastEvents/event_03.svg" alt="" />
              </div>
              <div class="col-8">
                <p class="date_color">2023/12/26</p>
                <h5>參與台北寵物論壇，爭取貓咪友善環境</h5>
                <p>
                  炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，
                  決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中， 每一隻貓咪都應該有自己的
                  VIP 休憩空間。
                </p>
              </div>
            </div>
          </div>
          <div class="col-4 mb-4">
            <button type="button" class="btn btn-info button_style">
              <div class="d-flex justify-content-center">
                <p>查看更多</p>
                <img src="@/assets/img/icons/arrow_forward.svg" alt="" />
              </div>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section> -->
  <!-- 政策議題 -->
  <!-- <section id="section3" class="text-secondary">
    <div class="row container block_policy_issues justify-content-center align-items-center">
      <div class="col-12">
        <div class="text-center">
          <img
            src="@/assets/img/policyIssues/policy_issues_tag.svg"
            alt=""
            width="146"
            height="35"
          />
        </div>
        <p class="font_mantouSans title text-center">政策議題</p>
      </div>
      <div class="col-12">
        <div class="row">
          <div class="col-4 event_content">
            <h4>
              為毛孩子謀福利！<br />
              推動寵物醫療保障方案
            </h4>
            <img src="@/assets/img/policyIssues/issue_01.svg" alt="" />
          </div>
          <div class="col-4 event_content">
            <h4>
              打造休閒天堂！<br />
              推廣寵物休閒與娛樂場所
            </h4>
            <img src="@/assets/img/policyIssues/issue_02.svg" alt="" />
          </div>
          <div class="col-4 event_content">
            <h4>推廣寵物飼養教育，讓愛更加專業<br /></h4>
            <img src="@/assets/img/policyIssues/issue_03.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section> -->
  <!-- 小額捐款 -->
  <!-- <section id="section4" class="text-secondary">
    <div class="row container block_last_events justify-content-center align-items-center">
      <div class="col-6">
        <div class="block bg-primary">
          <div class="row">
            <div class="col-12">
              <p class="font_mantouSans title">小額支持喵喵</p>
              <p class="sub_title">您的小筆捐款，是每隻毛孩未來的大大動力！</p>
            </div>
            <div class="col-12 p-0">
              <div class="row">
                <div class="col-5 align-self-end">
                  <button type="button" class="btn btn-info button_style">
                    <div class="d-flex justify-content-center">
                      <p>小額捐款</p>
                      <img src="@/assets/img/icons/arrow_forward.svg" alt="" />
                    </div>
                  </button>
                </div>
                <div class="col-7 img_container p-0">
                  <img class="img_cover" src="@/assets/img/donate/hand.svg" alt="">
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-6">
        <div class="block bg-secondary">
          <div class="row">
            <div class="col-12">
              <p class="font_mantouSans title">民眾服務信箱</p>
              <p class="sub_title">親愛的鄉親，每一位市民的意見都是我們社區前進的原動力</p>
            </div>
            <div class="col-12 p-0">
              <div class="row button_height">
                <div class="col-5 align-self-end">
                  <button type="button" class="btn btn-info button_style" data-bs-toggle="modal" data-bs-target="#voiceModal">
                    <div class="d-flex justify-content-center">
                      <p>填寫表單</p>
                      <img src="@/assets/img/icons/arrow_forward.svg" alt="" />
                    </div>
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section> -->
  <!-- 台灣的明天 口號 -->
  <!-- <section>
    <div class="row container block_slogan justify-content-center align-items-center">
      <div class="col-7 text-center">
        <p class="font_mantouSans title ">台灣的明天 喵先鋪路</p>
        <div>
          <img src="@/assets/img/mainPage/name_title.svg" width="433" height="84" />
        </div>
      </div>
    </div>
  </section> -->
  <!-- footer -->
  <!-- <footer class="text-secondary">
    <div class="row container-fluid p-0 m-0 bg_advpcate block_footer justify-content-center align-items-center">
      <div class="col-10">
        <div class="row">
          <div class="col-6">
            <img class="mb-2" src="@/assets/img/footer/name.svg" alt="" width="295" height="34">
            <div class="d-flex mb-2">
              <img class="me-2" src="@/assets/img/footer/fb_icon.svg" alt="" width="48" height="48">
              <img class="me-2" src="@/assets/img/footer/ig_icon.svg" alt="" width="48" height="48">
              <img src="@/assets/img/footer/yt_icon.svg" alt="" width="48" height="48">
            </div>
            <p>© 2023 喵立翰 Miao Li-Han 版權所有</p>
          </div>
          <div class="col-6">
            <h4>競選總部</h4>
            <p>
              辦公室地址：喵星區，毛茸茸大道88號，喵喵大樓3樓<br>
              電話：(02) 888-5678<br>
              電子郵件地址：meowoffice@linmeow.tw</p>
          </div>
        </div>
      </div>
    </div>
  </footer> -->
  
  <!-- modal -->
  <div class="modal fade" id="voiceModal" tabindex="-1" aria-labelledby="voiceModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-scrollable modal-xl modal_custom">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="voiceModalLabel">民眾服務信箱</h5>
          <button type="button" data-bs-dismiss="modal" aria-label="Close" class="cancel_button">
          </button>
        </div>
        <div class="modal-body">
          <div class="row">
            <div class="col-7 overflow-hidden">
              <img class="img_cover" src="@/assets/img/modal/mail.svg" alt="">
            </div>
            <div class="col-5">
              <div class="mb-3">
                <label for="form_name" class="form-label">您的姓名</label>
                <input type="text" class="form-control" id="form_name" placeholder="輸入姓名">
              </div>
              <div class="mb-3">
                <label for="form_email" class="form-label">Email</label>
                <input type="email" class="form-control" id="form_email" placeholder="email">
              </div>
              <div class="mb-3">
                <label for="form_mobile" class="form-label">手機</label>
                <input type="number" class="form-control" id="form_mobile" placeholder="手機號碼">
              </div>
              <div class="mb-3">
                <label for="form_voice" class="form-label">您的建言</label>
                <textarea class="form-control form_textarea" id="form_voice" rows="3"></textarea>
              </div>
              <button type="button" class="btn btn-primary button_custom">送出意見</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <RouterView />
</template>

<!-- <style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style> -->

<style lang="scss">
@import './assets/all.scss';
</style>

<style scoped>
.nav_padding {
  padding: 12px 24px;
}

.header_sticky {
  position: sticky;
  top: 0;
  z-index: 1;
}
nav {
  top: 10px;
  border-radius: 16px;
  height: 67px;
  margin: 10px;
}

/* 標題人物 */
.big_title_margin {
  margin-top: 97px;
}
.font_mantouSans {
  font-family: 'MantouSans';
}

.big_title {
  font-size: clamp(4rem, 6.5vw, 8.5rem);
  background: linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
  background: -webkit-linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
}
.marquee_title {
  font-size: 64px;
  color: white;
  background-color: #da7d4a;
  height: 87px;
  line-height: 87px;
  text-align: center;
}

.bg_advpcate {
  background-color: #f7ece1;
  padding: 104px;
  /* height: 731px; */
}

.marquee-container {
  width: 100%;
  overflow: hidden;
  display: flex;
}

.marquee-content {
  padding-left: 30px;
  display: inline-block;
  white-space: nowrap;
  animation: marquee 10s linear infinite;
}

.marquee-content2 {
  padding-left: 30px;
  display: inline-block;
  white-space: nowrap;
  animation: marquee2 10s linear infinite;
}
.marquee-content3 {
  padding-left: 30px;
  display: inline-block;
  white-space: nowrap;
  animation: marquee2 10s linear infinite;
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-100%);
  }
}

@keyframes marquee2 {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-100%);
  }
}
@keyframes marquee3 {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-100%);
  }
}

.block_advpcate {
  height: 100%;
  justify-content: center;
  align-items: center;
  .content_bg {
    max-width: 1320px;
    min-width: 343px;
    /* height: 523px; */
    background-color: #ffffff;
    border-radius: 24px;
  }
  .title {
    font-size: clamp(3rem, 6.5vw, 4rem);
    background: linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background: -webkit-linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }

  .sub_title {
    font-size: 24px;
    font-weight: 700;
  }

  .advpcate_text_container {
      padding: 20px 20px;
  }

  .advpcate_img_container {
    overflow: hidden;
    border-radius: 0 0 24px 24px;
    padding: 0;

    .img_cover {
      object-fit: cover;
      width: 100%;
    }
  }

  @media screen and (min-width : 1200px ){
    .advpcate_text_container {
      padding: 0 20px;
    }
    .advpcate_img_container {
      border-radius: 0 24px 24px 0;
    }
  }
}

.block_last_events {
  margin: 104px auto;

  .date_color {
    color: #94A3B8;
  }
  .img_container {
    overflow: hidden;
    border-radius: 16px;
  }
  .event_content {
    height: 134px;
    overflow: hidden;
    margin-bottom: 24px;
    border-radius: 8px;
  }
  .title {
    font-size: 64px;
    background: linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background: -webkit-linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }
  .button_style {
    width: 152px;
    border-radius: 50px;
    height: 64px;

    & p {
      margin: 0;
      margin-right: 0.5rem;
      font-size: 16px;
      color: #334155;
    }
  }
}

.block_policy_issues {
  margin: 104px auto;

  & h4 {
    font-size: 24px;
    line-height: 36px;
  }
  .title {
    font-size: 64px;
    background: linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background: -webkit-linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }
  .event_content {
    overflow: hidden;
    margin-bottom: 24px;
    border-radius: 24px;

    & img {
      width: 100%;
    }
  }
}

.block {
  height: 590px;
  width: 100%;
  border-radius: 32px ;
  padding: 96px;
  
  .title {
    color:#ffffff;
    font-size: 52px;
  }

  .sub_title {
    color:#ffffff;
    font-size: 20px;
  }

  .img_container {
    overflow: hidden;
  }

  .img_cover {
    object-fit: cover;
    width: 100%;
  }

  .button_height {
    height: 235.56px;
  }
}

.block_slogan {
  margin: 104px auto;
  .title {
    display: inline-block;
    white-space: nowrap;
    font-size: 64px;
    background: linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background: -webkit-linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }
}

.block_footer {
  height: 263px;
}

.modal_custom {
  .modal-content {
    border-radius: 24px;
  }
  .modal-header {
    border: 0;
    font-size: 32px;
    padding: 20px 40px;
  }
  .cancel_button {
    background: url(/src/assets/img/modal/cancel.svg);
    border: none;
    height: 30px;
    width: 30px;
    background-repeat: no-repeat;
    background-position: center;
  }

  .img_cover {
    object-fit: cover;
    width: 100%;
  }

  .modal-body {
    border: 0;
    padding: 6px 40px 40px;

    .form-label {
      font-size: 16px;
      font-weight: 700;
      margin-bottom: 0.25rem;
    }
    .form-control {
      background-color: #F1F5F9;
      height: 59px;
      border: 0;
      border-radius: 8px;
    }

    .form_textarea {
      height: 170px;
    }

    .button_custom {
      width: 100%;
      border-radius: 500px;
      height: 55px;
      color: white;
    }
  }
}

.img_container {
  overflow: hidden;
}

.img_cover {
  object-fit: cover;
  width: 100%;
}

.img_cover_70 {
  object-fit: cover;
  width: 70%;
}




</style>
