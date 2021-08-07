<template>
  <div>
    <div class="sec-box">
      <h2 class="sec-title">Test!<small>test</small></h2>
      <div class="input-group">
        <input
          type="text"
          maxlength="2"
          inputmode="numeric"
          pattern="^\d+$"
          value=""
          style="
            min-width: 10px;
            border-radius: 3px;
            margin-right: 3px;
            text-align: center;
          "
        /><input
          type="text"
          maxlength="2"
          inputmode="numeric"
          pattern="^\d+$"
          value=""
          style="
            min-width: 10px;
            border-radius: 3px;
            margin-right: 3px;
            text-align: center;
          "
        /><input
          type="text"
          maxlength="2"
          inputmode="numeric"
          pattern="^\d+$"
          value=""
          style="
            min-width: 10px;
            border-radius: 3px;
            margin-right: 3px;
            text-align: center;
          "
        /><input
          type="text"
          maxlength="2"
          inputmode="numeric"
          pattern="^\d+$"
          value=""
          style="
            min-width: 10px;
            border-radius: 3px;
            margin-right: 3px;
            text-align: center;
          "
        /><input
          type="text"
          maxlength="2"
          inputmode="numeric"
          pattern="^\d+$"
          value=""
          style="
            min-width: 10px;
            border-radius: 3px;
            margin-right: 3px;
            text-align: center;
          "
        /><input
          type="text"
          maxlength="2"
          inputmode="numeric"
          pattern="^\d+$"
          value=""
          style="
            min-width: 10px;
            border-radius: 3px;
            margin-right: 3px;
            text-align: center;
          "
        />
        <button style="border-radius: 3px">ค้นเลย!</button>
      </div>
      <div style="text-align: center">
        <br>
      </div>
    </div>
  </div>
</template>
<style scoped>
#content {
    padding: 80px 30px 20px;
}
div {
    display: block;
}
.sec-box {
  border-radius: 7px;
  padding: var(--space) var(--space) 4px;
  background: #0092d2;
  max-width: 450px;
  margin: 0 auto var(--space);
  color: #fff;
}
.sec-title {
  font-size: 1.5em;
  text-align: center;
  overflow: hidden;
  margin-bottom: 8px;
}
.input-group {
  display: flex;
  margin: 20px 0 0;
  width: 100%;
}
.sec-box .input-grid,
.sec-box .input-group {
  margin-bottom: 16px;
}
.sec-box {
  border-radius: 7px;
  padding: var(--space) var(--space) 4px;
  background: #0a0a0a;
  max-width: 450px;
  margin: 0 auto var(--space);
  color: #fff;
}

element.style {
  min-width: 10px;
  border-radius: 3px;
  margin-right: 3px;
  text-align: center;
}
.input-group input {
  min-width: 80px;
  border-radius: 3px 0 0 3px;
  flex: 1;
  -webkit-appearance: none;
  margin: 0;
}
input[type="color"],
input[type="date"],
input[type="datetime-local"],
input[type="datetime"],
input[type="email"],
input[type="month"],
input[type="number"],
input[type="password"],
input[type="search"],
input[type="tel"],
input[type="text"],
input[type="time"],
input[type="url"],
input[type="week"],
select,
textarea {
  outline: none;
  box-shadow: 0 0 0 transparent;
  padding: 6px 8px;
  border: 2px solid #fff;
  background-color: #000;
  background: linear-gradient(#fff, #fff);
  transition: 0.2s border-color ease-in-out;
  min-height: 36px;
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
  border-radius: 3px;
}
input,
textarea {
  font-size: 16px;
  -webkit-appearance: none;
}
</style>
