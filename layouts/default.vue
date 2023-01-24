<template>
    <div class="h-screen">
        <div class="navbar bg-base-300">
  <div class="navbar-start">
    <div class="dropdown">
      <label tabindex="0" class="btn btn-ghost lg:hidden">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" /></svg>
      </label>
      <ul tabindex="0" class="menu menu-compact dropdown-content mt-3 p-2 shadow bg-base-100 rounded-box w-52">
        <li><a>Item 1</a></li>
      
        <li><a>Item 3</a></li>
      </ul>
    </div>
    <a class="btn btn-ghost normal-case text-xl text-gray-100 font-bold">XII Rpl2</a>
  </div>
  <div class="navbar-center hidden lg:flex">
    <ul class="menu menu-horizontal px-1">
      <li><a class="text-gray-100 text-lg font-semibold">Siswa</a></li>
     
      <li><a class="text-gray-100 text-lg font-semibold">Rekap Absen</a></li>
     
      <li><a class="text-gray-100 text-lg font-semibold">Absen</a></li>
    </ul>
  </div>
  <div class="navbar-end">
    <a class="btn btn-sm bg-green-500 rounded-full text-gray-100 font-semibold text-center hover:bg-green-400">Masuk</a>
  </div>
</div>
        <slot/>
    </div>
</template>

<script>
  
</script>
