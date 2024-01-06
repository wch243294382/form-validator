<script setup lang="ts"></script>

<template>
  <div class="body">
    <div class="header">
      <label for="movie">Pick a movie：</label>
      <select id="movie">
        <option value="">The Lion King $4</option>
        <option value="">The Lion King2 $10</option>
        <option value="">The Lion King3 $12</option>
        <option value="">The Lion King4 $13</option>
      </select>
    </div>
    <div class="content">
      <ul>
        <li>
          <div class="seat"></div>
          <span>N/A</span>
        </li>
        <li>
          <div class="seat selected"></div>
          <span>Selected</span>
        </li>
        <li>
          <div class="seat unavailable"></div>
          <span>Unavailable</span>
        </li>
      </ul>
    </div>
    <div class="container">
      <div class="screen"></div>
      <div class="row">
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat selected"></div>
        <div class="seat"></div>
        <div class="seat"></div>
      </div>
      <div class="row">
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat unavailable"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
      </div>
      <div class="row">
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
      </div>
      <div class="row">
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
      </div>
      <div class="row">
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
      </div>
      <div class="row">
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
      </div>
      <div class="row">
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
      </div>
      <div class="row">
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
        <div class="seat"></div>
      </div>
    </div>
    <div class="footer">
      <p>
        You have selected <span id="count">0</span> seats for a price of $<span id="total">0</span>
      </p>
    </div>
  </div>
</template>

<style scoped lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  margin: 0;
  padding: 0;
  background-color: #242424;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  color: #f1f1f1;
  font-size: 20px;
  font-weight: bold;
  .header {
    display: flex;
    margin-bottom: 50px;
    select {
      padding: 3px;
      border-radius: 5px;
      appearance: none;
      // width: 130px;
    }
  }

  .content {
    margin-bottom: 50px;
    ul {
      display: flex;
      // align-items: between;
      justify-content: space-between;
      list-style-type: none;
      li {
        display: flex;
        .seat {
          width: 15px;
          height: 13px;
          margin: 5px;
          background-color: #f1f1f1;
          // border-radius: 5px;
          // border: 1px solid black;
          border-top-right-radius: 10px;
          border-top-left-radius: 10px;
          &.selected {
            background-color: green;
          }
          &.unavailable {
            background-color: red;
          }
        }
      }
    }
  }

  .container {
    // display: flex;

    margin-bottom: 50px;
    perspective: 1000px;
    .screen {
      background-color: #fff;
      width: 100%;
      height: 100px;
      margin: 20px 0;
      transform: rotateX(-45deg);
      box-shadow: 0 3px 10px rgba(255, 255, 255, 0.7);
    }
    .row {
      display: flex;
    }
    .seat {
      width: 15px;
      height: 13px;
      margin: 7px;
      border-top-right-radius: 10px;
      border-top-left-radius: 10px;
      background-color: #fff;
      &:not(.unavailable):hover {
        cursor: pointer;
        transform: scale(1.2);
      }
      &.selected {
        background-color: green;
      }
      &.unavailable {
        background-color: red;
      }
    }
  }
}
</style>
