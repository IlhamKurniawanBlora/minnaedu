<template>
    <div>
        <div class="border-b-4 border-gray-950">
            <div class="container max-w-6xl p-4 mx-auto">
                <LogoMinna />
            </div>
        </div>
        <header class="sticky top-0 z-20 flex justify-between border-b-4 divide-x-4 bg-white/90 backdrop-blur-sm border-gray-950 divide-gray-950">
            <nav class="flex justify-between w-full overflow-x-auto">
                <ul class="flex justify-start">
                    <li>
                        <a class="block px-6 py-6 transition whitespace-nowrap hover:text-indigo-500" href="#about">About Us</a>
                    </li>
                    <li>
                        <a class="block px-6 py-6 transition whitespace-nowrap hover:text-indigo-500" href="#speakers-talk">Leasson</a>
                    </li>
                    <li>
                        <a class="block px-6 py-6 transition whitespace-nowrap hover:text-indigo-500" href="#speakers-music">Testimonial</a>
                    </li>
                    <li>
                        <a class="block px-6 py-6 transition whitespace-nowrap hover:text-indigo-500" href="#" target="_blank">Teacher</a>
                    </li>
                    <li>
                        <a class="block px-6 py-6 transition whitespace-nowrap hover:text-indigo-500" href="/gallery">Gallery</a>
                    </li>
                    <!-- <li>
                        <div class="block px-6 py-6 text-gray-400 transition cursor-not-allowed whitespace-nowrap">Testimoni</div>
                    </li> -->
                </ul>
                <ul class="flex justify-start">
                    <li>
                        <a class="block px-6 py-6 transition whitespace-nowrap hover:text-pink-500" href="https://instagram.com/islamidotco" target="_blank">
                            <LogoFacebook :size="24" />
                        </a>
                    </li>
                    <li>
                        <a class="block px-6 py-6 transition whitespace-nowrap hover:text-sky-500" href="https://twitter.com/islamidotco" target="_blank">
                            <LogoInstagram :size="24" />
                        </a>

                    </li>
                    <li>
                        <a class="block px-6 py-6 transition whitespace-nowrap hover:text-red-500" href="https://youtube.com/islamidotco" target="_blank">
                            <LogoWhatsapp :size="24" />
                        </a>
                    </li>
                </ul>
            </nav>
            <nav>
                <ul class="flex justify-start divide-x-4 divide-gray-950 h-full">
                    <li class="overflow-hidden">
                        <a class="h-full flex px-6 py-6 space-x-2 transition bg-transparent rounded-none text-gray-950 whitespace-nowrap hover:bg-pink-500 hover:text-white
                        hover:scale-150 duration-300 delay-100 ease-in-out" href="#faqs">
                            <LogoQuestion />
                            <span class="hidden lg:inline">FAQ</span>
                        </a>
                    </li>
                    <li class="overflow-hidden">
                        <a class="h-full flex px-6 py-6 space-x-2 text-white transition whitespace-nowrap bg-gray-950 hover:bg-[#99C04A] hover:scale-150 duration-300 delay-100 ease-in-out" href="#" target="_blank">
                            <LogoStart :size="24" />
                            <span class="hidden lg:inline">Get Leasson</span>
                        </a>
                    </li>
                </ul>
            </nav>
        </header>
        <main>
            <slot />
        </main>
    </div>
</template>

<script setup>

</script>