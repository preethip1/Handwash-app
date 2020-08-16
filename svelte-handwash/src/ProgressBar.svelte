<script>
export let progress = 0;
</script>



<div class  = "grid">
        <div class = "progress-container" style = "width: {progress <= 100? progress : 100}%"> 
    <div class ="progress-bar" >
    </div> 
 </div>
</div>

<style>
    .progress-container{
        margin: 2%;
    }
    .progress-bar {
        height : 30px;
        background-color: greenyellow;
        
        border-radius: 20px;
    }
</style>