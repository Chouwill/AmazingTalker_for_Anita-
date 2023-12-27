<template>
    <main>
      <div class="containter">
        <div id="calendar"></div>
        <form action="#" id="bookPlanForm">
          <ul class="left_form">
            <li>
              <label for="themeInput">主題名稱:</label>
              <input type="text" id="themeInput" />
            </li>
            <li>
              <label for="planInput">計畫名稱:</label>
              <input type="text" id="planInput" />
            </li>
            <li>
              <select id="palnKind">
                <option value="">計畫分類</option>
                <option value="進修">進修</option>
                <option value="教育">教育</option>
                <option value="休閒">休閒</option>
                <option value="工作">工作</option>
              </select>
              <p id="planKind"></p>
            </li>
            <li>
              <select id="importantKind">
                <option value="">優先度</option>
                <option value="紅">紅</option>
                <option value="綠">綠</option>
                <option value="黃">黃</option>
                <option value="橙">橙</option>
              </select>
              <p id="importantKindOutput"></p>
            </li>
          </ul>
          <ul class="right_form">
            <li>
              <label for="unitInput">單元名稱:</label>
              <input type="text" id="unitInput" />
            </li>
            <li>
              <label for="unitLocalInput">單元目標:</label>
              <input type="text" id="unitLocalInput" />
            </li>
            <li>
              <label for="startInput">開始時間:</label>
              <input type="date" id="startInput" />
            </li>
            <li>
              <label for="endInput">結束時間:</label>
              <input type="date" id="endInput" />
            </li>
          </ul>
          <div class="sent">
            <input type="button" value="提交" onclick="submitForm()" />
          </div>
        </form>
        <div id="output">
          <p id="theme"></p>
          <p id="plan"></p>
          <p id="planKind"></p>
          <p id="importantKindOutput"></p>
          <p id="start"></p>
          <p id="end"></p>
          <p id="unit"></p>
          <p id="unitLocal"></p>
        </div>
      </div>
    </main>
    
  </template>
  
  <script setup>
  
</script>
  
  <style scoped>
 .containter {
    width: 100%;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
  #calendar {
    width: 50%;
    display: flex;
    justify-content: center;
  }
  form {
    display: flex;
    justify-content: center;
    width: 1500px;
    border: 5px solid teal;
    /* flex-wrap: wrap; */
  }
  </style>
  