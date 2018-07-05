<template>
	<div id="app">
		<vue-particles
	        color="#ffffff"
	        :particleOpacity="0.3"
	        :particlesNumber="120"
	        shapeType="star"
	        :particleSize="4"
	        linesColor="#ffffff"
	        :linesWidth="1"
	        :lineLinked="true"
	        :lineOpacity="0.4"
	        :linesDistance="150"
	        :moveSpeed="3"
	        :hoverEffect="true"
	        hoverMode="grab"
	        :clickEffect="true"
	        clickMode="push">
	    </vue-particles>
	    <!--"vue-particles": "^1.0.9",
	    color: String类型。默认'#dedede'。粒子颜色。
		particleOpacity: Number类型。默认0.7。粒子透明度。
		particlesNumber: Number类型。默认80。粒子数量。
		shapeType: String类型。默认'circle'。可用的粒子外观类型有："circle","edge","triangle", "polygon","star"。
		particleSize: Number类型。默认80。单个粒子大小。
		linesColor: String类型。默认'#dedede'。线条颜色。
		linesWidth: Number类型。默认1。线条宽度。
		lineLinked: 布尔类型。默认true。连接线是否可用。
		lineOpacity: Number类型。默认0.4。线条透明度。
		linesDistance: Number类型。默认150。线条距离。
		moveSpeed: Number类型。默认3。粒子运动速度。
		hoverEffect: 布尔类型。默认true。是否有hover特效。
		hoverMode: String类型。默认true。可用的hover模式有: "grab", "repulse", "bubble"。
		clickEffect: 布尔类型。默认true。是否有click特效。
		clickMode: String类型。默认true。可用的click模式有: "push", "remove", "repulse", "bubble"-->
	    <HelloWorld/>
	</div>
</template>

<script>
	import HelloWorld from './components/HelloWorld'

	export default {
		name: 'App',
		components: {
			HelloWorld
		},
	}
</script>

<style>
	body{
		overflow-x: hidden;
	}
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
	}
	.resumeStyle .noScroll pre {
		background-color: rgba(255,255,255,0);
	}
	#particles-js{
      position: fixed;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      width: 100%;
      height: 100%;
      background-repeat: no-repeat;
      background-size: cover;
      background-position: 50% 50%;
	}
</style>