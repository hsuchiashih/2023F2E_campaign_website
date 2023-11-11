<script setup>
   import { ref, nextTick } from 'vue';
   const isSend = ref(false);
   const clickForSend = () => {
      isSend.value = true;
   } 

   
   nextTick(() => {
    const voiceModal = document.getElementById('voiceModal')
    voiceModal.addEventListener('hidden.bs.modal', function () {
      isSend.value = false;
    })
  });
 
</script>
<script>

</script>
<template>
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
            <div class="col-12 col-lg-7 overflow-hidden mb-3">
              <img class="img_cover d-none d-lg-block" src="@/assets/img/modal/mail.svg" alt="">
              <img class="img_cover d-block d-lg-none" src="@/assets/img/modal/mobile_voice_man.svg" alt="">
            </div>
            <div v-if="!isSend" class="col-12 col-lg-5">
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
              <button 
                type="button"
                class="btn btn-primary button_custom"
                @click="clickForSend()"
                >送出意見
              </button>
            </div>
            <div v-else class="col-12 col-lg-5 align-self-center">
              <div class="row justify-content-center align-items-center">
                <div class="col-6 text-center">
                  <h3 class="finish_text">感謝您的意見</h3>
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
      font-size: 28px;
    }
  }
}
</style>
