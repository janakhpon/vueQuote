<template>
    <div class="row">
        <div class="col-sm-12">
            <h4 class="text-danger">QUOTES LIMIT IN PROGRESS</h4>
            <div class="progress">
                <div class="progress">
                    <div class="progress-bar progress-bar-striped bg-danger" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
                        :style="{width: (quoteCount / maxQuotes) * 100 + '%'}">
                        {{ quoteCount }} / {{ maxQuotes}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        props: ['quoteCount', 'maxQuotes']
    }
</script>


<style>

h4{
    font-weight: bold;
    font-family: 'Arizonia', cursive;
    
}

.progress-bar{
    background-color: #EE5A24;
}

</style>
