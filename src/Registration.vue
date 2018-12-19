<template>
    <form class="col s12">
        <div class="row">
            <div class="input-field col s6">
                <input v-model="firstName" placeholder="" id="first_name" type="text">
                <label for="first_name">First Name</label>
            </div>
            
            <div class="input-field col s6">
                <input v-model='lastName' id="last_name" type="text">
                <label for="last_name">Last Name</label>
            </div>
            
            <div class="input-field col s12">
                <input v-model="username" id="username" type="text" class="">
                <label for="username">Username</label>
            </div>
            
            <div class="input-field col s12">
                 <input v-model="email" id="email_address" type="text">
                 <label for="email_address">Email address</label>
            </div>
            <div class="input-field col s12">
                <input v-model="password" id="password" type="password">
                 <label for="password">Password</label>
            </div>
                                                    
            <a class="waves-effect waves-light btn teal form-btn">Register</a>
        </div>
    </form>
</template>


<script>
    export default {
        name: 'Register',   
        data(){
            return {
                first_name: '', 
                last_name: '', 
                username: '',
                email: '',
                password: '',
            }
        }
    }

</script>

<style scoped>
    .form-btn {
        position: absolute; 
        bottom: 0;
        right: 0;
        margin-top: 20px;
        margin-right: 20px; 
        margin-bottom: 20px;
    }
</style>
