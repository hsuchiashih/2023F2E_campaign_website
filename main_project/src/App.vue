<script setup>
import { onMounted, ref } from 'vue'
import { RouterView } from 'vue-router'
import VoiceModal from './components/VoiceModal.vue'
import DonateModal from './components/DonateModal.vue'
import LastEventModal from './components/LastEventModal.vue'
import PolicyIssueModal from './components/PolicyIssueModal.vue'
import AOS from 'aos';
import 'aos/dist/aos.css';

onMounted(() => {
  AOS.init({
    once: false, 
  })
});

const issueId = ref(1)
const clickIssue = ((id) => {
  issueId.value = id;
});
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
            <img src="@/assets/img/icons/fb_icon.svg " width="32" height="32" />
          </a>
          <a href="#" class="pe-3">
            <img src="@/assets/img/icons/ig_icon.svg " width="32" height="32" />
          </a>
          <a href="#">
            <img src="@/assets/img/icons/yt_icon.svg " width="32" height="32" />
          </a>
        </div>
      </div>
    </nav>
  </header>

  <!-- 固定footer -->
  <div class="fixed_footer container-fluid d-flex d-lg-none">
      <a class="nav-link px-2 px-md-5 active text-center" aria-current="page" href="#section1">
        <div>
          <img src="@/assets/img/fixed_footer/advpcate_icon.svg" alt="" />
          <p>候選人主張</p>
        </div>
      </a>
      <a class="nav-link px-2 px-md-5 text-center" href="#section2">
        <div>
          <img src="@/assets/img/fixed_footer/last_event_icon.svg" alt="" />
          <p>最新活動</p>
        </div>
      </a>
      <a class="nav-link px-2 px-md-5 text-center" href="#section3">
        <div>
          <img src="@/assets/img/fixed_footer/policy_issues_icon.svg" alt="" />
          <p>政策議題</p>
        </div>
      </a>
      <a class="nav-link px-2 px-md-5 text-center" href="#section4">
        <div>
          <img src="@/assets/img/fixed_footer/donate_icon.svg" alt="" />
          <p>小額捐款</p>
        </div>
      </a>
      <a class="nav-link px-2 px-md-5 text-center" href="#section4">
        <div>
          <img src="@/assets/img/fixed_footer/email_icon.svg" alt="" />
          <p>民眾服務信箱</p>
        </div>  
      </a>
  </div>
  <!-- 標題人物 -->
  <section>
    <div class="container big_title_margin">
      <div class="row">
        <div class="col-12 text-center pb-3">
          <p 
            class="font_mantouSans big_title d-none d-lg-block"
            data-aos="zoom-out"
            data-aos-duration="3000">台灣的明天 喵先鋪路</p>
          <div data-aos="zoom-out" data-aos-once="false" data-aos-duration="3000">
            <span class="font_mantouSans big_title d-lg-none">台灣的明天 </span>
            <br class="d-lg-none">
            <span class="font_mantouSans big_title d-lg-none">喵先鋪路</span>
          </div>
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
        <div class="col-12 text-center img_container" data-aos="fade-in" data-aos-duration="3000">
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
      <div class="row container m-auto block_advpcate" data-aos="fade-in" data-aos-duration="2000">
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
  <section id="section2" class="text-secondary">
    <div class="row container block_last_events justify-content-center align-items-start">
      <div class="col-12">
        <div class="text-center">
          <img src="@/assets/img/lastEvents/last_event_tag.svg" alt="" width="154" height="35" />
        </div>
        <p class="font_mantouSans title text-center">最新活動</p>
      </div>
      <div class="col-lg-12 col-xl-6" data-aos="fade-in" data-aos-duration="2000">
        <div class="row">
          <div class="col-12 img_container">
            <img class="img_cover" src="@/assets/img/lastEvents/main_event.svg" alt="" />
          </div>
          <div class="col-12 mt-2">
            <p class="date">2023/12/26</p>
            <h5>參與台北寵物論壇，爭取貓咪友善環境</h5>
            <p>
              炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，
              決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中， 每一隻貓咪都應該有自己的 VIP
              休憩空間。
            </p>
          </div>
        </div>
      </div>
      <div class="col-lg-12 col-xl-6">
        <div class="row">
          <div class="col-12" data-aos="slide-left" data-aos-duration="2000" data-os-delay="2000">
            <div class="row">
              <div class="col-4 event_content">
                <img class="img_cover" src="@/assets/img/lastEvents/event_01.svg" alt="" />
              </div>
              <div class="col-8">
                <p class="date">2023/12/24</p>
                <h5>掃街模式開啟！帶著你的貓耳，來和我一起走！</h5>
                <p class="multiline-ellipsis">
                  街上氣氛真的很棒，從小孩到大人，甚至有些狗狗朋友都帶著貓耳來找我握手，真的太可愛了！
                </p>
              </div>
            </div>
          </div>
          <div class="col-12" data-aos="slide-left" data-aos-duration="2000" data-os-delay="2200">
            <div class="row">
              <div class="col-4 event_content">
                <img class="img_cover"  src="@/assets/img/lastEvents/event_02.svg" alt="" />
              </div>
              <div class="col-8">
                <p class="date">2023/12/20</p>
                <h5>收容所模特兒大比拼！</h5>
                <p class="multiline-ellipsis">
                  今天的收容所不再是一片寂靜。為了讓更多人認識到這裡的毛孩子，我們舉辦了一場前所未有的「模特兒走秀」！
                </p>
              </div>
            </div>
          </div>
          <div class="col-12" data-aos="slide-left" data-aos-duration="2000" data-os-delay="2400">
            <div class="row">
              <div class="col-4 event_content">
                <img class="img_cover" src="@/assets/img/lastEvents/event_03.svg" alt="" />
              </div>
              <div class="col-8">
                <p class="date">2023/12/26</p>
                <h5>參與台北寵物論壇，爭取貓咪友善環境</h5>
                <p class="multiline-ellipsis">
                  炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，
                  決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中， 每一隻貓咪都應該有自己的
                  VIP 休憩空間。
                </p>
              </div>
            </div>
          </div>
          <div class="col-4 mb-4">
            <button type="button" class="btn btn-info button_style" data-bs-toggle="modal" data-bs-target="#lastEventModal">
              <div class="d-flex justify-content-center">
                <p>查看更多</p>
                <img src="@/assets/img/icons/arrow_forward.svg" alt="" />
              </div>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- 政策議題 -->
  <section id="section3" class="text-secondary">
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
          <div 
            class="col-12 col-lg-6 col-xl-4 event_content" 
            data-bs-toggle="modal"
            data-bs-target="#policyIssueModal"
            data-aos="fade-in"
            data-aos-duration="2000"
            data-os-delay="2000"
            @click="clickIssue(1)">
            <h4>
              為毛孩子謀福利！<br />
              推動寵物醫療保障方案
            </h4>
            <img src="@/assets/img/policyIssues/issue_01.svg" alt="" />
          </div>
          <div
            class="col-12 col-lg-6 col-xl-4 event_content"
            data-bs-toggle="modal"
            data-bs-target="#policyIssueModal"
            data-aos="fade-in"
            data-aos-duration="2000"
            data-os-delay="2200"
            @click="clickIssue(2)"
          >
            <h4>
              打造休閒天堂！<br />
              推廣寵物休閒與娛樂場所
            </h4>
            <img src="@/assets/img/policyIssues/issue_02.svg" alt="" />
          </div>
          <div
            class="col-12 col-lg-6 col-xl-4 event_content"
            data-bs-toggle="modal"
            data-bs-target="#policyIssueModal"
            data-aos="fade-in"
            data-aos-duration="2000"
            data-os-delay="2400"
            @click="clickIssue(3)">
            <h4>推廣寵物飼養教育，讓愛更加專業<br /></h4>
            <img src="@/assets/img/policyIssues/issue_03.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- 小額捐款 -->
  <section id="section4" class="text-secondary">
    <div class="row container block_last_events">
      <div class="col-12 col-md-6 mb-3">
        <div class="row block bg-primary">
          <div class="col-12">
            <p class="font_mantouSans title">小額支持喵喵</p>
            <p class="sub_title">您的小筆捐款，是每隻毛孩未來的大大動力！</p>
          </div>
          <div class="col-12">
            <div class="row">
              <div class="col-7 col-lg-6 align-self-end">
                <button type="button" class="btn btn-info button_style" data-bs-toggle="modal" data-bs-target="#donateModal">
                  <div class="d-flex justify-content-center">
                    <p>小額捐款</p>
                    <img src="@/assets/img/icons/arrow_forward.svg" alt="" />
                  </div>
                </button>
              </div>
              <div class="col-5 col-lg-6 img_container p-0">
                <img class="img_cover" src="@/assets/img/donate/hand.svg" alt="">
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-12 col-md-6 mb-3">
        <div class="row block bg-secondary">
          <div class="col-12">
            <p class="font_mantouSans title">民眾服務信箱</p>
            <p class="sub_title">親愛的鄉親，每一位市民的意見都是我們社區前進的原動力</p>
          </div>
          <div class="col-12 align-self-end">
            <div class="row">
              <div class="col-7 col-lg-6 align-self-end">
                <button type="button" class="btn btn-info button_style" data-bs-toggle="modal" data-bs-target="#voiceModal">
                  <div class="d-flex justify-content-center">
                    <p>填寫表單</p>
                    <img src="@/assets/img/icons/arrow_forward.svg" alt="" />
                  </div>
                </button>
              </div>
              <div class="col-5 col-lg-6 img_container p-0">
                <img class="img_cover" src="@/assets/img/voice/email.svg" alt="">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- 台灣的明天 口號 -->
  <section>
    <div class="row container block_slogan justify-content-center align-items-center">
      <div class="col-12 text-center">
          <p class="font_mantouSans title d-none d-lg-block"
            data-aos="slide-down"
            data-aos-duration="2000"
            data-os-delay="50">台灣的明天 喵先鋪路</p>
          <div>
            <span class="font_mantouSans title d-lg-none">台灣的明天 </span>
            <br class="d-lg-none">
            <span class="font_mantouSans title d-lg-none">喵先鋪路</span>
          </div>
        <div class="img_container">
          <img class="img_cover_50" src="@/assets/img/mainPage/name_title.svg"/>
        </div>
      </div>
    </div>
  </section>
  <!-- footer -->
  <footer class="text-secondary footer_padding">
    <div class="row container-fluid p-0 m-0 bg_advpcate block_footer justify-content-center align-items-center">
      <div class="col-10">
        <div class="row">
          <div class="col-12 col-md-6 mt-5">
            <img class="mb-2" src="@/assets/img/footer/name.svg" alt="" width="295" height="34">
            <div class="d-flex mb-2">
              <img class="me-2" src="@/assets/img/footer/fb_icon.svg" alt="" width="48" height="48">
              <img class="me-2" src="@/assets/img/footer/ig_icon.svg" alt="" width="48" height="48">
              <img src="@/assets/img/footer/yt_icon.svg" alt="" width="48" height="48">
            </div>
            <p>© 2023 喵立翰 Miao Li-Han 版權所有</p>
          </div>
          <div class="col-12 col-md-6 mt-5">
            <h4>競選總部</h4>
            <p>
              辦公室地址：喵星區，毛茸茸大道88號，喵喵大樓3樓<br>
              電話：(02) 888-5678<br>
              電子郵件地址：meowoffice@linmeow.tw</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
  
  <!-- modal -->
  <VoiceModal/>
  <DonateModal/>
  <LastEventModal/>
  <PolicyIssueModal :issue-id="issueId"/>
  <RouterView />
</template>

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
  & h5 {
    font-size: 16px;
  }
  .date {
    color: #94A3B8;
    margin: 0;
    margin-bottom: 8px;
  }
  .img_container {
    overflow: hidden;
    border-radius: 16px;
  }

  .img_cover {
    object-fit: cover;
    width: 100%;
    height: 100%;
    border-radius: 8px;
  }
  .event_content {
    /* height: 134px; */
    overflow: hidden;
    margin-bottom: 24px;
    border-radius: 8px;
    padding: 0;
  }
  .title {
    font-size: clamp(3rem, 6.5vw, 4rem);
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
    font-size: clamp(3rem, 6.5vw, 4rem);
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
    cursor: pointer;
    & img {
      width: 100%;
    }
  }
}

.block {
  width: 100%;
  height: 100%;
  border-radius: 32px ;
  padding: 40px 24px;
  
  .title {
    color:#ffffff;
    font-size: clamp(2.5rem, 4vw, 3.25rem);
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
    white-space: nowrap;
    font-size: clamp(3rem, 6.5vw, 4rem);
    background: linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background: -webkit-linear-gradient(90deg, #e6793b 1.54%, #ff4185 97.86%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }

  .img_container {
    overflow: hidden;
  }

  .img_cover {
    object-fit: cover;
    width: 50%;
    height: 100%;
  }

  @media screen and (min-width : 1200px ){
    .img_cover {
      width: 30%;
    }
  }
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
.img_cover_50 {
  object-fit: cover;
  width: 50%;
}
.img_cover_70 {
  object-fit: cover;
  width: 70%;
}



.multiline-ellipsis { 
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
  overflow: hidden;
}

/* footer */
.footer_padding {
  padding-bottom: 68px;
}
@media screen and (min-width : 992px ) {
  .footer_padding {
    padding-bottom: 0px;
  }

}

/* 固定footer */
.fixed_footer {
  width: 100%;
  position: fixed;
  bottom: 0;
  height: 68px;
  background-color: #F8FAFC;
  display: flex;
  justify-content: space-between;
  align-items: center;

  & p {
    margin: 0;
    font-size: 10px;
  }
}
</style>
<style src="wow.js/css/libs/animate.css"></style>