<template>
  <div class="modal fade" id="policyIssueModal" tabindex="-1" aria-labelledby="policyIssueModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-scrollable modal-xl modal_custom">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="policyIssueModalLabel">政策議題</h5>
          <button type="button" data-bs-dismiss="modal" aria-label="Close" class="cancel_button">
          </button>
        </div> 
        <div class="modal-body">
          <div class="row">
            <div class="col-12 col-lg-5 mb-5">
              <img class="img_cover" src="@/assets/img/policyIssues/issue_01.svg" alt="">
              <p>為毛孩子謀福利！推動寵物醫療保障方案</p>
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
                <h2>為毛孩子謀福利！推動寵物醫療保障方案</h2>
              </div>
              <div class="row event_text_block">
                <div class="col-12">
                  <h5>設立寵物醫療基金</h5>
                  <p>
                    每年撥款新台幣 10 億元，專款專用於支援家庭寵物的醫療費用
                  </p>
                </div>
                <div class="col-12">
                  <h5>提供醫療補助</h5>
                  <p>
                    每隻寵物每年可獲得高達新台幣 20,000 元的醫療補助，減輕飼主的經濟壓力
                  </p>
                </div>
                <div class="col-12">
                  <h5>合作動物醫院</h5>
                  <p>
                    目前已有和超過 200 家動物醫院進行初步的合作討論
                  </p>
                </div>
              </div>
              <div class="row events_container">
                <div class="col-12">
                  <p class="mt-3 title">更多政策議題</p>
                </div>
                <div class="col-12">
                  <div class="row">
                    <div class="col-4 event_item">
                      <img class="img_cover" src="@/assets/img/policyIssues/issue_02.svg" alt="">
                      <p>打造休閒天堂！推廣寵物休閒與娛樂場所</p>
                    </div>
                    <div class="col-4 event_item">
                      <img class="img_cover" src="@/assets/img/policyIssues/issue_03.svg" alt="">
                      <p>推廣寵物飼養教育，讓愛更加專業</p>
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
    padding: 30px 0;
    color:#334155;
    & h5 {
      font-size: 20px;
      font-weight: 700;
    }
    & p {
      font-size: 18px;
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
