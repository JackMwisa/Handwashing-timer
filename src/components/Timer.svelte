<script>

    import ProgressBar from "./ProgressBar.svelte"

</script>



<style>
.start {
    background-color: rgb(rgb(236, 89, 89)(87, 43, 43), green, blue);
    width: 100%;
    margin: 10px 0;
}    

</style>

<div bp="grid">

    <h2 bp="offset-5@md 4@md 12@sm">

        Seconds Left:

    </h2>


</div>

<ProgressBar />


<button class="start">Start</button>