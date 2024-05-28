<template>
     <div 
           
            id="TopNav" 
            class="w-full flex items-center justify-between md:pt-2.5 md:px-2.5"
        >
            <div class="flex items-center justify-between md:rounded-full md:shadow-sm px-2 md:pl-6 pl-4 py-[8px] bg-[#cbb05b] w-full border-b border-[#cbb05b]">
                <div class="flex items-center justify-start w-full max-w-[500px]">
                    <NuxtLink to="/">
                        <img 
                            class="w-[30px] min-h-[32px] mb-2 object-cover min-w-[30px] select-none" 
                            src="~/assets/images/jewerly.png"
                        >
                    </NuxtLink>

                    <div v-for="link in links" class="lg:px-2.5 px-0.5 md:block hidden">
                        <a
                            :href="link.url" 
                            class="flex items-center text-md font-semibold px-1.5 py-3 rounded-lg"
                        >
                            <Icon 
                                :name="link.icon" 
                                class="mr-0.5" 
                                size="20" 
                                
                            />
                            <div class="text-black">
                                {{ link.name }}
                            </div>
                        </a>
                    </div>

                </div>

                <div class="flex items-center justify-between gap-3">
                    <button class="flex items-center text-sm font-semibold p-2 rounded-full hover:bg-gray-100">
                        <Icon name="healthicons:megaphone-outline" class="mr-0.5"  size="22"/>
                    </button>

                    <button class="flex items-center font-semibold px-3 py-2 rounded-full bg-gray-100">
                        <Icon name="mdi:lightning-bolt" class="mr-0.5"  size="18"/>
                        Upgrade
                    </button>

                    <button class="flex items-center font-semibold px-3 py-2 rounded-full border hover:bg-gray-100">
                        <Icon name="teenyicons:upload-solid" class="mr-1.5"  size="18"/>
                       Compartilhar
                    </button>
                    
                    <button 
                        @click="!isTopNav ? openMenu('TopNav') : isTopNav = false"
                        class="rounded-full md:block hidden"
                    >
                        <img 
                            class="rounded-full min-w-[40px] w-[40px]"
                            src="~/assets/images/user-placeholder.png"
                        >
                    </button>

                </div>
            </div>
            <div
                v-if="isTopNav"
                class="
                    absolute 
                    md:block
                    hidden
                    right-4 
                    top-16 
                    border 
                    shadow-[0_5px_15px_15px_rgba(0,0,0,0.1)] 
                    bg-white 
                    w-full 
                    max-w-[300px] 
                    rounded-2xl
                "
            >   
                <button
                    @click="logout()"
                    class="w-full flex items-center text-gray-600 text-[15px] p-3 hover:text-black"
                >
                    <Icon name="circum:logout" class="mr-6" />
                    Sign out
                </button>
            </div>
        </div>
</template>

<script setup>
let isTopNav = ref(false)

const links = ref([
    { name: 'Home', url: '#', icon: 'mdi:home-outline' },
    { name: 'A Marca', url: '#brand', icon: 'mdi:tag-outline' },
    { name: 'Produtos', url: '#produtos', icon: 'mdi:cart-outline' },
    { name: 'Contato', url: '#contato', icon: 'mdi:contacts-outline' },
])

const openMenu = (str) => {
    if (str === 'TopNav') {
        isTopNav.value = true
    } 
}

</script>

