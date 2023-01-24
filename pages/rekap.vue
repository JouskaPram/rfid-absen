<template>
    <div>
        <div class="flex flex-wrap justify-between my-3">

            <h3 class="my-3 text-2xl font-bold px-10 text-gray-100">Siswa XII RPL 2</h3>
            <div class="form-control">
      <div class="input-group px-10">
        <input type="text" placeholder="Search…" class="input input-bordered" />
        <button class="btn btn-square bg-green-500">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" /></svg>
        </button>
      </div>
    </div>
        </div>
        <div class="overflow-x-auto px-10 ">
       <table class="table w-full   ">
        <thead>
            <tr class="text-lg font-semibold text-gray-100   ">
                <td>No kartu</td>
                <td>Nama</td>
                <td>Kelas</td>
                <td>Jurusan</td>
                <td>Jam masuk</td>
                
            </tr>
        </thead>
        <tbody>
            <tr v-for="item in items" :key="item.id " class="border-b border-gray-800 text-gray-200">
                <td>{{ item.siswa.no_kartu }}</td>
                <td>{{ item.siswa.nama }}</td>
                <td>{{ item.siswa.kelas }}</td>
                <td>{{ item.siswa.jurusan }}</td>
                <td>{{ item.masuk }}</td>
            </tr>
        </tbody>
       </table>
    </div>
    </div>
</template>

<script setup>
 const supabase = useSupabaseClient()
 const items = ref()
 async function getdata(){
    const {data,error}= await supabase.from('rekapitulasi').select('masuk,siswa(no_kartu,nama,kelas,jurusan)')
    items.value = data
 }
 onMounted(()=>{
    getdata()
 })
</script>
