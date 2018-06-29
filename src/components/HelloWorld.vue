<template>
  <div class="box"></div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
@ly_width: 100px;
@ly_height: 100px;
.border-radius (@radius: 50%) {
  -webkit-border-radius: @radius;
  -moz-border-radius: @radius;
  border-radius: @radius;
}

.box-shadow (@x: 0px, @y: 3px, @blur: 5px, @alpha: 0.5) {
  -webkit-box-shadow: @x @y @blur rgba(0, 0, 0, @alpha);
  -moz-box-shadow: @x @y @blur rgba(0, 0, 0, @alpha);
  box-shadow: @x @y @blur rgba(0, 0, 0, @alpha);
}

.transition (@prop: all, @time: 1s, @ease: linear) {
  -webkit-transition: @prop @time @ease;
  -moz-transition: @prop @time @ease;
  -o-transition: @prop @time @ease;
  -ms-transition: @prop @time @ease;
  transition: @prop @time @ease;
}

.transform (@rotate: 90deg, @scale: 1, @skew: 1deg, @translate: 10px) {
  -webkit-transform: rotate(@rotate) scale(@scale) skew(@skew) translate(@translate);
  -moz-transform: rotate(@rotate) scale(@scale) skew(@skew) translate(@translate);
  -o-transform: rotate(@rotate) scale(@scale) skew(@skew) translate(@translate);
  -ms-transform: rotate(@rotate) scale(@scale) skew(@skew) translate(@translate);
  transform: rotate(@rotate) scale(@scale) skew(@skew) translate(@translate);
}

.gradient (@origin: left, @start: #ffffff, @stop: #000000) {
  background-color: @start;
  background-image: -webkit-linear-gradient(@origin, @start, @stop);
  background-image: -moz-linear-gradient(@origin, @start, @stop);
  background-image: -o-linear-gradient(@origin, @start, @stop);
  background-image: -ms-linear-gradient(@origin, @start, @stop);
  background-image: linear-gradient(@origin, @start, @stop);
}

.box {
  width: @ly_width;
  height: @ly_height;
  background: #3cc;
  .border-radius(50%);
  .box-shadow(5px, 5px, 6px, 0.3);
  .transition(all, 0.5s, ease-in);
  .transform(5deg, 0.5, 1deg, 0px);
  .gradient(left, #663333, #333333);
}

.box:hover {
  opacity: 0;
}

</style>
