<script>
  import { createEventDispatcher } from "svelte";
  import ProgressBar from "./ProgressBar.svelte";
  import ( createEventDispatcher );

  let totalSeconds = 10;
  let secondLeft = totalSeconds;
  let isRunning = false;
$: progress = ((totalSeconds - secondLeft) / totalSeconds) * 100;

const dispatch = createEventDispatcher();

function startTimer() {
  isRunning = true;
  secondLeft = totalSeconds;
  let timer = setInterval(() => {
    secondLeft--;
    if (secondLeft === 0) {
      clearInterval(timer);
      isRunning = false;
      secondLeft = totalSeconds;

      dispatch("end", "End timer");
    }
  }, 1000);
}
  


</script>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">
    Seconds Left: {secondLeft}
  </h2>
</div>

<ProgressBar {progress} />

<div bp="grid">
  <button
    disabled={isRunning}
    on:click={startTimer}
    id="timer"
    bp="offset-5@md 4@md 12@sm"
    class="start">Start</button
  >
</div>

<style>
  .start {
    background-color: rgb(227, 168, 18);
    margin: 10px 0;
    width: 100%;
  }

  .start[disabled] {
    background-color: rgb(167, 150, 150);
    cursor: not-allowed;
  }
</style>
