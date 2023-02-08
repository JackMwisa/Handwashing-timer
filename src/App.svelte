<script>
  import HowTo from "./components/HowTo.svelte";
  import Timer from "./components/Timer.svelte";

  let audio;

import Text from "./components/Timer.svelte";
</script>


<style>
	h1, 
	h3 {
		text-align: center;
	}
</style>
<h1>Handwashing App</h1>


<Timer />
<HowTo />


<h3>
	<a href="https://www.pig333.com/articles/how-to-wash-your-hands-properly_15917/">Picture source</a>
</h3>


<h3>
	<a href="https://freesound.org/people/metrostock99/sounds/345086/">Sound source</a>
</h3>


<audio bind:this={audio} src="">

	<source src=""/>

</audio>