<script setup>
   import { ref, nextTick } from 'vue';
   const isSend = ref(false);
   const clickForSend = () => {
      isSend.value = true;
   } 

   nextTick(() => {
    const donateModal = document.getElementById('donateModal')
    donateModal.addEventListener('hidden.bs.modal', function () {
      isSend.value = false;
    })
  });
 
</script>
<script>

</script>
<template>
  <div class="modal fade" id="donateModal" tabindex="-1" aria-labelledby="donateModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-scrollable modal-xl modal_custom">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="donateModalLabel">小額捐款</h5>
          <button type="button" data-bs-dismiss="modal" aria-label="Close" class="cancel_button">
          </button>
        </div>
        <div class="modal-body">
          <div class="row">
            <div class="col-12 col-xl-7 overflow-hidden mb-3">
              <img class="img_cover d-none d-xl-block" src="@/assets/img/modal/donate.svg" alt=""> 
              <img class="img_cover d-block d-xl-none" src="@/assets/img/modal/mobile_donate.svg" alt="">
            </div>
            <div v-if="!isSend" class="col-12 col-xl-5">
              <h5 class="text-start">捐款方案</h5>
              <div class="mb-2">
                <input type="radio" name="colorSelector" id="radio_primary_level_1" value="pink"/>
                <label class="mx-0" for="radio_primary_level_1">
                  <div class="row h-100 justify-content-center align-items-center">
                    <div class="col-12 col-lg-4">
                      <h5 class="text-primary mb-4 m-lg-0">喵星人之友</h5>
                    </div>
                    <div class="col-12 col-lg-8">
                      <div class="row align-items-center">
                        <div class="col-6 text-start text-lg-end">
                          <span class="me-2">NT$</span>
                          <span class="text_donate_moeny">600</span>
                        </div>
                        <div class="col-6 text-end">
                          <span class="text_donate_count">已有 9,957 人贊助</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </label>
              </div>
              <div class="mb-2">
                <input type="radio" name="colorSelector" id="radio_primary_level_2" value="pink"/>
                <label class="mx-0" for="radio_primary_level_2">
                  <div class="row h-100 justify-content-center align-items-center">
                    <div class="col-12 col-lg-4">
                      <h5 class="text-primary mb-4 m-lg-0">喵星大使</h5>
                    </div>
                    <div class="col-12 col-lg-8">
                      <div class="row align-items-center">
                        <div class="col-6 text-start text-lg-end">
                          <span class="me-2">NT$</span>
                          <span class="text_donate_moeny">6,000</span>
                        </div>
                        <div class="col-6 text-end">
                          <span class="text_donate_count">已有 2,000 人贊助</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </label>
              </div>
              <div class="mb-2">
                <input type="radio" name="colorSelector" id="radio_primary_level_3" value="pink"/>
                <label class="mx-0" for="radio_primary_level_3">
                  <div class="row h-100 justify-content-center align-items-center">
                    <div class="col-12 col-lg-4">
                      <h5 class="text-primary mb-4 m-lg-0">喵星傳奇</h5>
                    </div>
                    <div class="col-12 col-lg-8">
                      <div class="row align-items-center">
                        <div class="col-6 text-start text-lg-end">
                          <span class="me-2">NT$</span>
                          <span class="text_donate_moeny">60,000</span>
                        </div>
                        <div class="col-6 text-end">
                          <span class="text_donate_count">已有 999 人贊助</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </label>
              </div>
              <div class="mb-2">
                <input type="radio" name="colorSelector" id="radio_primary_level_4" value="pink"/>
                <label class="mx-0" for="radio_primary_level_4">
                  <div class="row h-100 justify-content-center"> 
                    <div class="col-12">
                      <h5 class="text-primary mb-4 m-lg-0">自訂贊助金額</h5>
                      <input type="number" class="form-control custom_input" id="form_name" placeholder="輸入金額">
                    </div>  
                  </div>
                </label>
              </div>
              <button 
                type="button"
                class="btn btn-primary button_custom"
                @click="clickForSend()"
                >前往捐款
              </button>
            </div>
            <div v-else class="col-12 col-xl-5 align-self-center">
              <div class="row justify-content-center align-items-center">
                <div class="col-12 text-center">
                  <h3 class="finish_text">感謝您的捐款</h3>
                </div>
                <div class="col-6">
                  <div>
                    <img class="img_cover finish_img_margin" src="@/assets/img/modal/finish.svg" alt="">
                  </div>
                  <button 
                    type="button"
                    class="btn btn-info form_close_button_custom"
                    data-bs-dismiss="modal" 
                    >關閉
                  </button>
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

    .form_close_button_custom {
      width: 100%;
      border-radius: 500px;
      height: 51px;
    }

    .finish_img_margin {
      margin: 32px 0;
    }

    .finish_text {
      margin-top: 20px ;
      font-size: 28px;
      text-align: center;
    }

    & input[type="radio"] {
      position: relative;
      display: none;
    }

    & input[type="radio"] + label {
      width: 100%;
      margin: 8px;
      padding: 22.5px 13.5px;
      border-radius: 25px;
      position: relative;
    }

    & input[type="radio"]#radio_primary_level_1 + label,
      input[type="radio"]#radio_primary_level_2 + label,
      input[type="radio"]#radio_primary_level_3 + label,
      input[type="radio"]#radio_primary_level_4 + label
    {
      background-color: #ffffff80;
      border: 2px solid #E2E8F0;
    }

    & input[type="radio"]#radio_primary_level_1:hover + label,
      input[type="radio"]#radio_primary_level_1:checked + label,
      input[type="radio"]#radio_primary_level_1:focus + label,
      input[type="radio"]#radio_primary_level_2:hover + label,
      input[type="radio"]#radio_primary_level_2:checked + label,
      input[type="radio"]#radio_primary_level_2:focus + label,
      input[type="radio"]#radio_primary_level_3:hover + label,
      input[type="radio"]#radio_primary_level_3:checked + label,
      input[type="radio"]#radio_primary_level_3:focus + label,
      input[type="radio"]#radio_primary_level_4:hover + label,
      input[type="radio"]#radio_primary_level_4:checked + label,
      input[type="radio"]#radio_primary_level_4:focus + label
    {
      cursor: pointer;
      background-color: #ffffff;
      border: 2px solid #DA7D4A;
    }

    .text_donate_moeny {
      font-size: 24px;
      font-family: 700;
    }

    .text_donate_count {
      font-size: 14px;
      color: #94A3B8;
    }

    .custom_input {
      width: 100%;
    }
  }
}
</style>
