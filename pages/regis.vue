<template>
    <div>
        <form @submit.prevent="masuk()">      
            <input type="text" v-model="email" class="input w-full max-w-xs">
            <input type="password" v-model="password" class="input w-full max-w-xs">
            <button type="submit" class="btn btn-info">daftar</button>
        </form>
    </div>
</template>

<script setup>
const supabase = useSupabaseAuthClient()
const email = ref()
const password = ref()

async function masuk(){
    const {user,error} = await supabase.auth.signUp({
        email : email.value,
        password : password.value,
    })
    console.log(user)
}

</script>

