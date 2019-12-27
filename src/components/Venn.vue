<template>
  <div style="background-color:red" class="flex flex-center">
    <div class="full-width text-center">
      <div class="venn-header" style="margin-bottom:12px;">
        <div v-for="(person,index) in people" :key="index" class="venn-header-item">
          <div class="venn-image-holder">
            <div :style="`background-image:url('${person[0]}')`"></div>
          </div>
          <div class="venn-text-holder">{{person[1]}}</div>
        </div>
      </div>

      <div class="venn-diagram">
        <div class="venn-circle-a">
          <span>{{a}}</span>
        </div>
        <div class="venn-circle-b">
          <span>Both of the above</span>
          <span>{{b}}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // name: 'ComponentName',
  data () {
    return {
      people: [
        ['Hi', 'lol']
      ],
      a: 'xd',
      b: 'lol'
    }
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Lato&display=swap");
* {
  box-sizing: border-box;
  color: white;
  font-family: "Lato", sans-serif;
}
body {
  background-color: red;
}
.venn-header {
  text-align: center;
  padding-top: 8px;
  padding-bottom: 8px;
}
.venn-header-item {
  text-align: center;
  margin-left: 24px;
  margin-right: 24px;
  width: 200px;
  display: inline-block;
}
.venn-image-holder {
  animation: test 0.6s linear;
  position: relative;
  z-index: 40;
  margin-left: 30px;
  height: 140px;
  width: 140px;
  -webkit-clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  background-color: white;
}
@keyframes test {
  0% {
    transform: rotate(-90deg) scale(0);
  }
  100% {
    transform: rotate(0) scale(1);
  }
}
.venn-image-holder div {
  display: inline-block;
  margin-top: 4px;
  height: 132px;
  width: 132px;
  background-color: white;
  background-size: cover;
  -webkit-clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}
.venn-text-holder {
  animation: xd 0.6s linear;
  overflow: hidden;
  white-space: nowrap;
  position: relative;
  z-index: 80;
  margin-top: -12px;
  height: 31px;
  background-color: red;
  max-width: 200px;
  display: inline-block;
  padding: 4px;
  padding-left: 8px;
  padding-right: 8px;
  border: 2px solid white;
  box-shadow: 0 0 8px 2px #fff inset, 0 0 8px 2px #fff;
}
@keyframes xd {
  0% {
    max-width: 0;
  }
  100% {
    max-width: 200px;
  }
}
.venn-diagram {
  text-align: center;
  padding-top: 8px;
  padding-bottom: 8px;
}
.venn-circle-a {
  animation: lol 0.6s linear;
  display: inline-block;
  vertical-align: middle;
  height: 250px;
  width: 250px;
  border-radius: 100%;
  border: 2px solid yellow;
  /* box-shadow: 0 0 8px 4px yellow; */

  box-shadow: 0 0 8px 2px yellow inset, 0 0 8px 2px yellow;
}
.venn-circle-a span {
  animation: lol2 1.2s linear;
  margin-top: 50px;
  /* margin-left:25px; */
  height: 150px;
  width: 150px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 4px;
}
.venn-circle-b {
  animation: lol 0.6s linear;
  text-align: left;
  margin-left: -100px;
  display: inline-block;
  vertical-align: middle;
  height: 250px;
  width: 250px;
  border-radius: 100%;
  border: 2px solid aqua;
  box-shadow: 0 0 8px 2px aqua inset, 0 0 8px 2px aqua;
}
.venn-circle-b span:last-child {
  animation: lol2 1.2s linear;
  vertical-align: top;
  margin-top: 50px;
  /* margin-left:90px; */
  text-align: center;
  height: 150px;
  width: 150px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 4px;
}
.venn-circle-b span:first-child {
  animation: lol2 1.2s linear;
  vertical-align: top;
  text-align: center;
  margin-top: 50px;
  margin-left: 0px;
  height: 150px;
  width: 90px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 4px;
}
@keyframes lol {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
@keyframes lol2 {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
