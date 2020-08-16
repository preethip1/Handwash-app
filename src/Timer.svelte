<script>
  import ProgressBar from "./ProgressBar.svelte";
  const totalSeconds = 2;
  let secondsLeft = totalSeconds;
  $: progress = ((totalSeconds - secondsLeft) * 100) / totalSeconds;

  function startTimer() {
    let timer = setInterval(() => {
      secondsLeft = secondsLeft - 1;
      if (secondsLeft < 0) {
        clearInterval(timer);
        alert("Yayy! Your hands are clean now!");
      }
    }, 1000);
  }
  function isRunning() {
    if (isRunning == 0) {
      clearInterval(intervalID);
      return;
    }
  }
</script>

<style>
  .start {
    background-color: lightblue;
    width: 100%;
    margin: 2%;
    border-radius: 20px;
  }
</style>

<div class="secondsLeft">secondsLeft: {secondsLeft >=0 ? secondsLeft : 0}</div>
<ProgressBar {progress} />
<button on:click={startTimer} class="start">start</button>
