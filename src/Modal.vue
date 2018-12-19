<template>
    <div class="modal-mask" v-if='show_modal' @click='closeModal'>
        <div class="modal-container" @click.stop>
            <slot> <slot>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Modal',
        props: ['show_modal', 'choice'],
        data(){
            return {
                
            }
        },
        
        methods:{
            closeModal(){
                this.$emit('close_modal', false)
            },

        }
    }
  
</script>


<style scoped>
   .modal-mask{
        position: fixed;
        z-index: 100; 
        top: 0; 
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, .3);
        overflow-y:auto;
    }
    .modal-container {
        width: 80%;
        height: auto;
        margin: 50px auto 0;
        position: relative;
        padding: 16px;
        background-color: #fff;
        border-radius: 2px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
        box-sizing: border-box;
    }

</style>