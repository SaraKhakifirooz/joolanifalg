<template>
    <div class="w-[300px] mt-[1%] mr-[1%]">
        <div class="service-box">
            <div class="service-icon grey">
                <div class="front-content">
                    <img :src="FlagCountryprops.svg" :alt="FlagCountryprops.commonName">
                    <i class="fa fa-trophy"></i>
                    <h3>{{ FlagCountryprops.commonName }}</h3>
                </div>
            </div>
            <div class="service-content">
                <h3>{{ FlagCountryprops.commonName }}</h3>
                <p> {{ FlagCountryprops.OfficialName }} </p>
                <router-link :to="{  name: 'CountryDetailsView',  params: { name: FlagCountryprops.OfficialName }  }">
                    More Details
                </router-link>
            </div>
        </div>
    </div>
</template>


<script setup lang="ts">

interface FlagProps {
    id:number;
    svg: string;
    commonName?: string;
    OfficialName: string;
}

const FlagCountryprops = defineProps<FlagProps>()

// interface FlagProps {
//     svg: string;
//     commonName: string;
//     OfficialName: string;
// }

// const FlagCountryprops = defineProps({
//     svg: {
//         type: String as PropType<FlagProps>
//     }
// })

// const FlagCountryprops = withDefaults(defineProps<FlagProps>(), {
//     svg: "",
//     commonName: "Sara";
    
// })

</script>