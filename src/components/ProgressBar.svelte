<script>

    export let progress = 0;


</script>


<style>
    .progress-container{
        margin: 20px 0;
        border: solid #5a91c8 1px;
    }

    .progress-bar{
        height: 30px;
        background-color: rgb(31, 73, 64);
        
    }
</style>



<div bp="grid">

    <div bp="offset-5@md 4@md 12@sm" class="progress-container">

        <div class="progress-bar" role="progressbar"  style="width: {progress}%; background-color:blueviolet; padding: 10px; margin-bottom: 5px">
            <span class="sr-only">% {progress}

            </span>
        </div>
        </div>

</div>


