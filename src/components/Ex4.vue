<script>
    export default { 
        data() {
            return {
                // Add code here
                id: 'demo1',
                current: 'blue',
                isActive: true
            }
        },
        methods: { 
   			// Add code here
            changeColor(){
                this.isActive = !this.isActive
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class="m-2" v-bind:class="{'blueBox':isActive, 'redBox':!isActive}">
        <!-- <div v-bind:id="id" class="m-2"> -->

            div ID : {{id}} 
        </div>
        
        <button type="button" v-bind:class="{'btn btn-primary': isActive, 'btn btn-danger':!isActive}" v-on:click="changeColor()">Change Color</button>
        <!-- <button type="button" v-if="current=='blue'" v-bind:class="{'blueBox': isActive}" v-on:click="changeColor()">Change Color</button>
        <button type="button" v-if="current=='red'" v-bind:class="{'redBox': isActive}" v-on:click="changeColor()">Change Color</button> -->

    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
