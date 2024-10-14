# --001_html
使用django建立可以至資料庫檢測資訊的會員填寫介面HTML

<div id="content-main">
  <form action="/myapp/joininformation/" method="post" id="registration-form">
    <input type="hidden" name="csrfmiddlewaretoken" value="{{ csrf_token }}">

  {% comment %} <form action="/myapp/logtest/" method="post" id="registration-form">
    <input type="hidden" name="csrfmiddlewaretoken" value="2Baz5JCBY7h9m82r89WWluOJO7v2LUQotcz2TjRQusKswHoA1jwbDVDLwexmKsSy"> {% endcomment %}
    <div class="form-row">

      <div class="form-row">
        <label for="id_account" class="account">會員帳號：</label>
        <input type="account" name="account" id="id_account">
        <span id="account-check" style="color:red;"></span>
      </div>

      <div class="form-row">
        <label for="id_password" class="required">會員密碼：</label>
        <input type="password" name="password" required id="id_password">
        <span id="password-check" style="color:red;"></span>
      </div>

      <div class="form-row">
          <label for="id_last_name" class="required">姓氏：</label>
          <input type="text" name="last_name" maxlength="50" required id="id_last_name">
      </div>

      <div class="form-row">
          <label for="id_first_name" class="required">名字：</label>
          <input type="text" name="first_name" maxlength="50" required id="id_first_name">
      </div>

      <div class="form-row">
          <label for="id_date_of_birth" class="required">生日：</label>
          <input type="date" name="date_of_birth" required id="id_date_of_birth">
      </div>

      <div class="form-row">
          <label for="id_mobile_phone" class="required">手機：</label>
          <input type="tel" name="mobile_phone" maxlength="15" required id="id_mobile_phone">
      </div>

      <div class="form-row">
          <label for="id_email_address" class="required">電子郵件：</label>
          <input type="email" name="email_address" maxlength="100" id="id_email_address">
      </div>

      <div class="form-row">
          <label for="id_national_id" class="required">身分證字號：</label>
          <input type="text" name="national_id" maxlength="10" required id="id_national_id">
      </div>

      <div class="form-row">
          <label for="id_address">地址：</label>
          <input type="text" name="address" maxlength="100" id="id_address">
      </div>

      <div class="form-row">
          <label for="id_sex">性別：</label>
          <select name="sex" id="id_sex">
              <option value="Male">男</option>
              <option value="Female">女</option>
              <option value="Other">其他</option>
          </select>
      </div>

      <div class="form-row">
          <label for="id_favorite_cinema">最常去的影城：</label>
          <select name="favorite_cinema" id="id_favorite_cinema">
            <option value="shin_kong">新光影城</option>
            <option value="vienshow">華納威秀</option>
            <option value="ambassedor">國賓影城</option>
            <option value="show_time">秀泰影城</option>
            <option value="miranew">美麗新影城</option>
            <option value="mira">大直美麗華</option>
        </select>
      </div>

      <div class="form-row">
          <label for="id_education">教育程度：</label>
          <select name="education" id="education">
            <option value="primary_school">小學</option>
            <option value="junior_high_school">國中</option>
            <option value="high_school">高中</option>
            <option value="university">大學</option>
            <option value="graduate">研究所</option>
            <option value="doctoral">博士班</option>
        </select>
      </div>

      <div class="form-row">
          <label for="id_occupation">職業：</label>
          <input type="text" name="occupation" maxlength="100" id="id_occupation">
      </div>

      <div class="form-row">
          <label for="id_marital_status">婚姻狀況：</label>
          <select name="marital_status" id="id_marital_status">
              <option value="Single">單身</option>
              <option value="Married">已婚</option>
          </select>
      </div>

      <div class="form-row">
          <label for="id_household_income">年收入：</label>
          <select name="household_income" id="id_household_income">
              <option value="four_down">40萬以下</option>
              <option value="four_six">41萬~60萬</option>
              <option value="six_eight">61萬~80萬</option>
              <option value="eight_onemillion">81萬~100萬</option>
              <option value="onemillion_twomillion">100萬~200萬</option>
              <option value="rich">200萬以上</option>
        </select>
      </div>

      <div class="form-row">
        <label for="id_favorite_genres">喜好電影類型：</label>
        <div id="favorite_genres">
            <label><input type="checkbox" name="f_genres_1" value="Action"> 動作片 Action</label><br>
            <label><input type="checkbox" name="f_genres_2" value="Adventure"> 冒險片 Adventure</label><br>
            <label><input type="checkbox" name="f_genres_3" value="Animation"> 動畫片 Animation</label><br>
            <label><input type="checkbox" name="f_genres_4" value="Art House"> 藝術片 Art House</label><br>
            <label><input type="checkbox" name="f_genres_5" value="Comedy"> 喜劇片 Comedy</label><br>
            <label><input type="checkbox" name="f_genres_6" value="Crime"> 犯罪片 Crime</label><br>
            <label><input type="checkbox" name="f_genres_7" value="Documentary"> 紀錄片 Documentary</label><br>
            <label><input type="checkbox" name="f_genres_8" value="Drama"> 劇情片 Drama</label><br>
            <label><input type="checkbox" name="f_genres_9" value="Family"> 家庭片 Family</label><br>
            <label><input type="checkbox" name="f_genres_10" value="Horror"> 恐怖片 Horror</label><br>
            <label><input type="checkbox" name="f_genres_11" value="Children"> 兒童片 Children</label><br>
            <label><input type="checkbox" name="f_genres_12" value="Kung Fu"> 功夫片 Kung Fu</label><br>
            <label><input type="checkbox" name="f_genres_13" value="Musical"> 音樂劇 Musical</label><br>
            <label><input type="checkbox" name="f_genres_14" value="Romance"> 文藝愛情片 Romance</label><br>
            <label><input type="checkbox" name="f_genres_15" value="Science Fiction"> 科幻片 Science Fiction</label><br>
            <label><input type="checkbox" name="f_genres_16" value="Thriller"> 驚悚懸疑片 Thriller</label><br>
        </div>
      </div>

      <div class="form-row">
        <label for="id_preferences">喜好的座位：</label>
        <div id="preferences">
          <label><input type="checkbox" name="seat_1" value="aisle"> 靠走道 aisle Seat</label><br>
          <label><input type="checkbox" name="seat_2" value="back"> 後方 back</label><br>
          <label><input type="checkbox" name="seat_3" value="front"> 前方 front</label><br>
          <label><input type="checkbox" name="seat_4" value="middle"> 中間 middle</label><br>
        </div>
      </div>

      <div class="submit-row">
          <input type="submit" value="提交">
      </div>



  </form>
</div>
{{email_exists}}
{% comment %} 以下可以槓掉____________________________________________________________________________________________________________ {% endcomment %}
資料狀態：{{res}}
<br>
{% if res == "OK" %}
    {{idn}}<br>
    {{pwn}}<br>
    {{acc_num}}<br>
    {{pw_num}}<br>
    {{lst_str}}<br>
    {{first_str}}<br>
    {{birth_str}}<br>
    {{phone_num}}<br>
    {{email_str}}<br>
    {{national_num}}<br>
    {{address_str}}<br>
    {{sex_str}}<br>
    {{f_cinema}}<br>
    {{education_str}}<br>
    {{occ_str}}<br>
    {{marital_str}}<br>
    {{income_num}}<br>
    {{l_f_genres}}<br>
    {{l_f_seat}}
{% endif %}


<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
  $(document).ready(function(){
      // 檢查帳號
      $('#id_account').on('input', function(){
          let account = $(this).val();
          let accountError = $('#account-check');
          let regex = /^(?=.*[A-Z])[A-Za-z0-9]{8,}$/;  // At least 1 uppercase, no special characters, min 8 characters
          if (!regex.test(account)) {
            accountError.text('帳號包含至少一個大寫字母且長度至少8個字，且無特殊符號');
          } else {
          // 發送 AJAX 請求檢查帳號
            $.ajax({
              url: '{% url "check_account" %}',  // Django URL
              method: 'GET',
              data: { 'account': account },  // 傳送帳號
              success: function(response){
                  if (response.account_exists) {
                    accountError.text('這個帳號已經被使用');
                  } else {
                    accountError.text('可以使用');
                  }
              }
          });

        }
      });

    // Password Validation (at least 1 uppercase, min 8 characters)
    $('#id_password').on('input', function() {
      let password = $(this).val();
      let passwordError = $('#password-check');
      let regex = /^(?=.*[A-Z])[A-Za-z0-9]{8,}$/;  // At least 1 uppercase, no special characters, min 8 characters
      if (!regex.test(password)) {
          passwordError.text('密碼包含至少一個大寫字母且長度至少8個字，且無特殊符號');
      } else {
          passwordError.text('可以使用');
      }
  });

  });
</script>










