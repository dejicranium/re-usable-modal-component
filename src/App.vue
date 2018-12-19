<template>
    <div>   
        <button v-on:click="actShowModal('login')"> Login </button>
        <button v-on:click="actShowModal('register')"> Register </button>
        
        <modal :show_modal="showModal" @close_modal='actCloseModal' choice='choice'>
            <login v-if="choice == 'login'"> </login>
            <register v-else-if="choice == 'register'"></register> 
        </modal>
    </div>
</template>

<script>
    import Login from "./Login.vue";
    import Registration from "./Registration.vue";
    import Modal from "./Modal.vue";
    
    export default{
        name: 'App',
        components: {
            "register": Registration,
            "login": Login, 
            "modal": Modal,
        },
        data(){
            return {
                showModal: false,
                 choice: '',
            }
        },
        methods: {
            actShowModal(choice){
                this.showModal = true;
                this.choice = choice;
            },
            actCloseModal(newValue){
                this.showModal = newValue;
            },
        }
        
    }

</script>
