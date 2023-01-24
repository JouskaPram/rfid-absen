<template>
    <div>
    <form @submit.prevent="tambahsiswa()">
      <input type="text" v-model="no_kartu">
      <input type="text" v-model="nama">
      <input type="text" v-model="kelas">
      <input type="text" v-model="jurusan">
      <button type="submit">Tambah</button>
    </form>
    </div>
</template>

<script setup>
const supabase = useSupabaseClient()
const no_kartu = ref()
const nama = ref()
const kelas = ref()
const jurusan = ref()

async function tambahsiswa(){
  const {data,error} = await supabase.from('siswa').insert({
    no_kartu : no_kartu.value,
    nama : nama.value,
    kelas : kelas.value,
    jurusan : jurusan.value,

  })
  navigateTo("/")
}
</script>
