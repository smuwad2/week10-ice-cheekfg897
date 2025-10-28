<script>
    // TODO: Complete the code
    export default { 
        data() {
            return {
                
            }
        },
        // Hint: insert properties task (Object) and idx (Number)
        props: {
            task: Object,
            idx: Number,
        },
        emits: [
            'removeTask'
    ]
    }
</script>

<template>
    <!-- TODO: add your template code here --> 
   <div class="card" style="width: 18rem;">
    <h2>Deadline: {{ task.deadline }}</h2>
  <div class="card-body">
    <p class="card-text">{{ task.desc }}</p>
    <button class="btn btn-primary" @click="$emit('removeTask', idx)">Done</button>
  </div>

</div>
</template>


