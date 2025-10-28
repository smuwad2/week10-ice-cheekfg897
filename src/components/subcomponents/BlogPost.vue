<script>
    export default {
        // Add code if/as necessary
        // Hint: Add properties subject, entry and mood
        
        props: {
            id: String,
            subject: String,
            entry: String,
            mood: String
        },
        computed:{
            imgSrc(){
                return '/assets/{this.mood.toLowerCase()}.png'
            }
        }

    }
</script>


<template>
    <!-- TODO: add your template code here. Use boostrap card --> 
        <div class="card">
            <slot name="img">
                <img class="card-img-top" src=imgSrc>
                
            </slot>
        <div class="card-body">
            <h2><slot name="subject"></slot></h2>
            <p><slot name="entry"></slot></p>
        </div> 
    </div>
</template>

