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
                return `/assets/${this.mood.toLowerCase()}.png`
            }
        }

    }
</script>


<template>
    <!-- TODO: add your template code here Use boostrap card --> 
    <div class="card">
            <slot name="img">
                <img class="card-img-top" :src=imgSrc>
                
            </slot>
            <div class="card-body">
                <h2>{{ subject }}</h2>
                <p>{{ entry }}</p>
            </div> 
            
            <slot name ="delete"></slot>
    </div>
</template>

