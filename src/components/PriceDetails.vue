<script setup>
import { defineProps } from 'vue';

const props = defineProps(['option']);


</script>

    
<template>
    <div class="card-body">
    <div class="price pb-1">
        <p> {{ option.name }}</p>
        <h3 class="flex"><span class="">Icon Sets</span><span class="">{{ option.price }}</span></h3>
    </div>
    <div class="details">
    <div class="pb-1" id="description">{{ option.description }} </div>
        <div class="checklist">
            <ul>
                <li v-for="item in option.options" :key="item.text">
            <svg v-if="item.checked" class="checked" width="16" height="12" viewBox="0 0 16 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<path  d="M5.43431 11.7643L0.234305 6.53442C-0.0781016 6.22021 -0.0781016 5.71077 0.234305 5.39654L1.36565 4.25865C1.67806 3.94442 2.18462 3.94442 2.49703 4.25865L6 7.78174L13.503 0.235652C13.8154 -0.0785507 14.3219 -0.0785507 14.6344 0.235652L15.7657 1.37353C16.0781 1.68774 16.0781 2.19718 15.7657 2.51141L6.56569 11.7644C6.25325 12.0786 5.74672 12.0786 5.43431 11.7643Z" fill="#4E47A5"/>
</svg> <svg v-else class="unchecked" width="16" height="12" viewBox="0 0 16 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M1.3787 0.235652L0.247353 1.37353C-0.0650532 1.68774 -0.0650532 2.19718 0.247353 2.51141L6.56569 8.76431C6.8781 9.07855 7.38462 9.07855 7.69703 8.76431L13.503 2.51141C13.8154 2.19718 13.8154 1.68774 13.503 1.37353L12.3716 0.235652C12.0592 -0.0785507 11.5527 -0.0785507 11.2403 0.235652L7 4.51826L2.7597 0.235652C2.44729 -0.0785507 1.94077 -0.0785507 1.62836 0.235652Z" fill="#FF0000"/>
<path d="M14.6213 11.7643L15.7526 10.6265C16.065 10.3123 16.065 9.80282 15.7526 9.48859L9.43431 3.23569C9.1219 2.92145 8.61538 2.92145 8.30297 3.23569L2.49703 9.48859C2.18462 9.80282 2.18462 10.3123 2.49703 10.6265L3.62836 11.7643C3.94077 12.0786 4.44729 12.0786 4.7597 11.7643L9 7.48174L13.2403 11.7643C13.5527 12.0786 14.0592 12.0786 14.3716 11.7643Z" fill="#FF0000"/>
</svg>{{ item.text }}</li>
            </ul>
        </div>
    </div>

    <div class="footer pt-2 center">
        <button class="pt-1 pb-1">Add to Cart</button>
    </div>
 </div>

</template>


<style scoped>

</style>