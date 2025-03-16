<template>
    <Header></Header>
    <div class="absolute mt-48 scale-100 w-full sm:left-64 sm:w-[calc(100%-256px)] sm:scale-100">
        <slot />
        <br><br><br><br><br><br><br><br>
        <footer class="block text-center">
            <hr class="bg-blue-300 bg-gradient-to-rfrom-blue-100 to-green-100">
            © All rights reserved by KazuKita.
        </footer>
    </div>

</template>