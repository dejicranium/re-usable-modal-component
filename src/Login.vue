<template id="login-template">
    <div>
        <h4 class="blue-text">Login</h4>
        <form class="col s12">
             <div class="row">
                <div class="input-field col s12">
                    <input v-model='email' id="email_address" type="text">
                    <label for="email_address">Email Address</label>
                 </div>
            
                <div class="input-field col s12 ">
                    <input v-model='password' id="password" type="text" >
                   <label for="password">Password</label>
                </div>
                
                <a class="waves-effect waves-light btn form-btn teal">Sign in</a>
        </form>  
    </div>       
</template>
    
    
<script>
    export default{
        name: 'Login',
        data(){
            return {
                email: '',
                password: '',
            }
        },
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