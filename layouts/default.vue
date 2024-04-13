<template>
    <div>
        <CommonTopMenu class="fixed w-full top-0 z-50"/>
        <CommonNavbar class="fixed w-full mt-[70px] top-0 z-50" />
        <div class="mt-[200px]  min-h-screen">
            <slot  />

        </div>
        <CommonFooter/>
    </div>
</template>

<script setup>

</script>