<script setup>
import { ref } from 'vue'
import img_main_event from '@/assets/img/lastEvents/main_event.svg'
import img_event_01 from '@/assets/img/lastEvents/event_01.svg' 
import img_event_02 from '@/assets/img/lastEvents/event_02.svg' 
const eventList = ref([
  {
    id: '1',
    title:'參與台北寵物論壇，爭取貓咪友善環境',
    img: img_main_event,
    date: '2023/12/26',
    context: '炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中，每一隻貓咪都應該有自己的 VIP 休憩空間。'
  },
  {
    id: '2',
    title:'掃街模式開啟！帶著你的貓耳，來和我一起走！',
    img: img_event_01,
    date: '2023/12/24',
    context: '街上氣氛真的很棒，從小孩到大人，甚至有些狗狗朋友都帶著貓耳來找我握手，真的太可愛了！'
  },
  {
    id: '3',
    title:'收容所模特兒大比拼！',
    img: img_event_02,
    date: '2023/12/20',
    context: '今天的收容所不再是一片寂靜。為了讓更多人認識到這裡的毛孩子，我們舉辦了一場前所未有的「模特兒走秀」！'
  },
]);

const clickEvent = ((eventIndex) => {
  let list = JSON.parse(JSON.stringify(eventList.value))
  const swapElements = (array, index1, index2) => {
    let temp = array[index1];
    array[index1] = array[index2];
    array[index2] = temp;

    return array
};
eventList.value = swapElements(list, 0, eventIndex)
});
</script>

<template>
  <div class="modal fade" id="lastEventModal" tabindex="-1" aria-labelledby="lastEventModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-scrollable modal-xl modal_custom">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="lastEventModalLabel">最新活動</h5>
          <button type="button" data-bs-dismiss="modal" aria-label="Close" class="cancel_button">
          </button>
        </div> 
        <div class="modal-body">
          <div class="row">
            <div class="col-12 col-lg-5 mb-5">
              <img class="img_cover" :src="require(`@/assets/img/lastEvents/${eventList[0].img}`)" alt="">
              <p>{{ eventList[0].title }}</p>
              <div class="d-flex">
                <p class="align-self-center m-0 pe-2">分享</p>
                <a href="#" class="pe-2">
                  <img src="@/assets/img/icons/fb_icon.svg " width="32" height="32" />
                </a>
                <a href="#" class="pe-2">
                  <img src="@/assets/img/icons/ig_icon.svg " width="32" height="32" />
                </a>
                <a href="#" class="pe-2">
                  <img src="@/assets/img/icons/line_icon.svg " width="32" height="32" />
                </a>
                <a href="#">
                  <img src="@/assets/img/icons/twitter_icon.svg " width="32" height="32" />
                </a>
              </div>
            </div>
            <div class="col-12 col-lg-7">
              <div class="event_title">
                <h2>{{ eventList[0].title }}</h2>
                <p>{{ eventList[0].date }}</p>
              </div>
              <div class="event_text_block">
                <p>
                  {{ eventList[0].context }}
                </p>
              </div>
              <div class="row events_container">
                <div class="col-12">
                  <p class="mt-3 title">更多活動</p>
                </div>
                <div class="col-12">
                  <div class="row">
                    <div class="col-4 event_item" @click=clickEvent(1)>
                      <img class="img_cover" :src="require(`${eventList[1].img}`)" alt="">
                      <p>{{ eventList[1].title }}</p>
                    </div>
                    <div class="col-4 event_item" @click=clickEvent(2)>
                      <img class="img_cover" :src="require(`${eventList[2].img}`)" alt="">
                      <p>{{ eventList[2].title }}</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
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
    object-fit: 100%;
    width: 100%;
  }
  .modal-body {
    border: 0;
    padding: 6px 40px 40px;

  }
  .event_title {
    & h2 {
      font-size: 32px;
      font-weight: 700;
      color: #DA7D4A;
    }

    & p {
      font-size: 14px;
      font-weight: 400;
      color: #94A3B8;
    }
  }
  .event_text_block {
    height: 144px;
    & p {
      font-size: 16px;
      color:#334155;
    }
  }
  .events_container {
    background-color: #F8FAFC;
    border-radius: 12px;
    .title {
      font-size: 16px;
      font-weight: 600;
      color:#334155;
    }

    .event_item {
      cursor: pointer;
      color:#334155;
      font-size: 14px;
    }

    .event_item:hover {
      .img_cover {
        width: 105%
      }  
    }
  }
}
</style>
