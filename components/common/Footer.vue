<template>
    <footer class="bg-white shadow-lg  border-2  py-8 mt-8">
        <div class="container mx-auto grid grid-cols-1 md:grid-cols-5 gap-4 mb-8">
            <div class="text-center col-span-1">
                <img src="@/assets/image/icon-footer.png" alt="icon" class="" />
                <p class="mt-4 text-justify">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
                    labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
                    laboris nisi ut aliquip ex ea commodo consequat.
                </p>
            </div>

            <div class="md:col-span-3 col-span-3">
                <div class="grid grid-cols-3 gap-4">
                    <div v-for="(menu, index) in menus" :key="index" class="col-span-1">
                        <h3 class="text-lg font-semibold mb-2 text-[#1b51a1]">{{ menu.name }}</h3>
                        <ul>
                            <li v-for="(menuItem, menuItemIndex) in menu.items" :key="menuItemIndex">{{ menuItem }}</li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="col-span-1">
                <ul class="mt-4">
                    <li class="mb-2 flex">
                        <p class="font-semibold">Address:</p>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
                            labore et dolore magna aliqua.</p>
                    </li>
                    <li class="mb-2 flex">
                        <p class="font-semibold">Phone:</p>
                        <p>+12345677898</p>
                    </li>
                    <li class="mb-2 flex">
                        <p class="font-semibold">Email:</p>
                        <p>info@example.com</p>
                    </li>
                    <li class="mt-2 flex justify-between">
                        <img src="@/assets/svg/facebook.svg" alt="facebook Icon" class="w-8">
                        <img src="@/assets/svg/linkedin.svg" alt="linkedin Icon" class="w-8">
                        <img src="@/assets/svg/twitter.svg" alt="twitter Icon" class="w-8">
                        <img src="@/assets/svg/youtube.svg" alt="youtube Icon" class="w-8">
                        <img src="@/assets/svg/instagram.svg" alt="instagram Icon" class="w-8">
                    </li>
                </ul>
            </div>
        </div>
        <div class="container text-center border-dashed border-t-2 border-t-[#1b51a1] text-gray-500 p-4 mx-auto">
            <p>@2024 Agency.All Right Reserved.</p>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            menus: [
                { name: ' Community', items: ['Events', 'Mentoring', 'Jobs', 'Free Lancering', 'Learn Drop Shipping'] },
                { name: ' B2B', items: ['Hosting', 'cloud', 'Hiring'] },
                { name: ' Seller', items: ['Business Phone', 'SMS Panel', 'Web Hosting'] },
                { name: 'B2C', items: ['Website', 'Marketing', 'Service', 'Adminstrative', 'executive assistance'] },
                { name: 'PSP', items: ['Tell-Communcation', 'E-commerce', 'Marketing'] },
                { name: 'Menu', items: ['About Us', 'Privaty Policy', 'Terms of Use', 'FAQ'] }
            ]

        };
    },
};
</script>

<style scoped></style>