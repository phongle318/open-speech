<template>
  <div class="container">
    <!--input form-->
    <div class="section">
        <div class="row demo-background">
            <div class="col s12 center cyan-text darken-4-text">
              <h4 class="header">Demo</h4>
            </div>
          <form class="col s12" method="POST">
              <div class="section">
                <h5 class="h5-demo">Giọng đọc:</h5>
                <div class="row">
                  <div  class="col s12 m12">
                    <div class="input-field">
                      <div class="col s2 m2">
                        <input name="gender" type="radio" id="female" value="female" class="voice"/>
                        <label for="female">Nữ miền Bắc (DungLTT)</label>
                      </div>
                      <div class="col s2 m2">
                        <input name="gender" type="radio" id="male" value="male" class="voice"/>
                        <label for="male">Nam miền Bắc (ChungHC)</label>
                      </div>
                      <div class="col s2 m2">
                        <input name="gender" type="radio" id="hatieumai" value="hatieumai" class="voice"/>
                        <label for="hatieumai">Nữ miền Nam (Hà Tiểu Mai)</label>
                      </div>

                    </div>
                  </div>
                  <div class="col input-field s12 m12">
                    <div class="m6">
                      <input name="prosody" type="checkbox" id="prosody" value="1"/>
                      <label for="prosody">Thêm ngữ điệu cho câu hỏi</label>
                    </div>
                  </div>
                  <div class="col input-field s12 m12">
                    <h5 class="h5-demo">Tốc độ đọc:</h5>
                    <div class="m6">
                      <div style="max-width: 20%">
                          <p class="range-field">
                              <input type="range" name="speed" id="speed" min="-3" max="3"/>
                          </p>
                      </div>
                    </div>
                  </div>
                  <div class="col input-field s8 m8">
                    <h5 class="h5-demo">Nhập văn bản:</h5>
                    <div class="m6">
                      <div class="col s12 m9">
                        <textarea id="text" name="text" class="materialize-textarea h5-demo" length="500">
                        </textarea>
                      </div>
                    </div>
                  </div>
                  <div class="col input-field s8 m8">
                    <div class="col s12 m3">
                      <button class="btn waves-effect waves-light red darken-2" type="submit" name="action">Đọc
                          <i class="material-icons right">send</i>
                      </button>
                    </div>
                    <div class="col s12 m6">
                      <div id="loading" class="progress">
                        <div class="indeterminate"></div>
                      </div>
                      <div id="audio">
                        <audio id="myAudio" controls="true" autoplay="true">
                        </audio>
                      </div>
                    </div>
                  </div>
                  <div class="col s12 m9 cyan-text darken-4-text">
                    Để tích hợp vào ứng dụng của bạn và tăng giới hạn đến 2000 kí tự/request,<br/>
                    mời bạn <a target="_blank" href="http://dev.openfpt.vn">đăng kí tài khoản developer</a>
                    và <a target="_blank" href="http://doc.openfpt.vn/#api-fpt-speech-synthesis-version-4-0-update-09-06-2017">dùng API theo hướng dẫn</a>
                  </div>
                </div>
              </div>
          </form>
      </div>
    </div>
    <div class="section">
      <h5>Tổng quan</h5>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>
<<style>
.demo-background{
  background-image:url('./assets/demo-background.png');
  background-size: auto;
  background-repeat: no-repeat;
  background-position: center;
  background-color: #000;
}
.h5-demo{
  color:#e9e9e9;
}
</style>

