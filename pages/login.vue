<template>
    <div>
        <form @submit.prevent="masuk()">      
            <input type="email" v-model="email" class="input w-full max-w-xs">
            <input type="password" v-model="password" class="input w-full max-w-xs">
            <button type="submit" class="btn btn-info">Masuk</button>
        </form>
    </div>
</template>

<script setup>
const supabase = useSupabaseAuthClient()
const email = ref()
const password = ref()

async function masuk(){
    const {error} = await supabase.auth.signInWithPassword()
    console.log(user)
}

</script>

