<template >
     <div class="card flex f-column">
        <div class="card-header grid grid-three" @click="changeOption($event)">
            <div  class="option" id="basic">
                   Basic 
            </div>
            <div  id="standard" class="option selected">
                  Standard
            </div>
            <div class="option" id="premium">
                Premium
            </div>
        </div>
        <PriceDetails :option="pricingOptions[0][currentOption]" />
    </div>
</template>
<script setup>
import {ref} from 'vue';
import PriceDetails from './components/PriceDetails.vue';
const currentOption = ref('standard');
const pricingOptions = [{   standard:{name:"Standard",
                            price:"$120",
                                    description:"Up to 100 creative & professional icons + two color version/themes per month",
                                    options:[{text:'Included Source files',checked:true},{text:'Converted to responsive componnet', checked:true}]},
                            basic:{name:"Basic",
                                    price:"$80",
                                    description:"Up to 50 creative & professional icons + one color version/themes",
                                    options:[{text:'Included Source files',checked:true},{text:'Converted to responsive componnet', checked:false}]}, 
                            premium:{name:"Premium",
                                    price:"$240",
                                    description:"Unlimited creative & professional icons + unlimited color version/themes per month",
                                    options:[{text:'Included Source files',checked:true},{text:'Converted to responsive componnet', checked:true}]}
                        }]
                                  
const changeOption = (e)=>{
    console.log(e.target.classList)
    if(e.target.classList.contains('option')){
        e.target.parentNode.childNodes.forEach(element => {element.classList.remove('selected')});
        e.target.classList.add('selected');
        currentOption.value = e.target.id;
    }
}
</script>

<style scoped>

</style>