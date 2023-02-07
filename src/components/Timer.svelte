<script>
  import ProgressBar from "./ProgressBar.svelte";

  let totalSeconds = 20;
  let secondLeft = totalSeconds;

function startTimer() {
    let timer = setInterval(() => {
        secondLeft--;
        document.getElementById("timer").innerHTML = secondLeft;
        if (secondLeft === 0) {
            clearInterval(timer);
            document.getElementById("timer").innerHTML = "Time's up!";
        }
    }, 1000);
}


  let timer = setInterval(() => {
    secondLeft--;
    if (secondLeft === 0) {
      clearInterval(timer);
    }
     
  }, 1000);


</script>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">
    Seconds Left: {secondLeft}
  </h2>
</div>

<ProgressBar />

<div bp="grid">
  <button id="timer" bp="offset-5@md 4@md 12@sm" class="start">Start</button>
</div>

<style>
  .start {
    background-color: rgb(227, 168, 18);
    margin: 10px 0;
    width: 100%;
  }
</style>
