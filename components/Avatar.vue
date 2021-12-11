<template>
    <div class="bg-gray-100 p-4 rounded text-center">
        <img :src="Info.avatar" class="w-36 h-auto rounded-full mx-auto" />
        <div class="my-2">
            <div class="font-bold text-slate-700">{{fullName}}</div>
            <div class="font-bold text-slate-400 text-sm my-2">{{Info.userName}}</div>
        </div>
        <div class="my-2">
            <a v-for="(socical,index) in Info.socicals" :key="socical.name" :href="socical.link" target="_blank" v-bind:class='index ? "ml-4": ""'>
                <span>
                    <component :is="socical.icon" :class="socical.class" />
                </span>
                <span>/</span>
                <span>{{socical.userName}}</span>
            </a>
        </div>
    </div>
</template>
<script>
import facebookIcon from "../assets/svg/facebook.svg?inline";
import githubIcon from "../assets/svg/github.svg?inline";
export default {
    computed: {
        fullName(){
            return `${this.Info.lastName} ${this.Info.firstName}`
        }
    },
    data(){
        return{
            Info: {
                avatar: '/images/Ily1606.jpg',
                lastName: 'Tuong Nguyen',
                firstName: 'Nguyen',
                userName: 'Ily1606',
                socicals:[
                    {
                        link: 'https://facebook.com/Ily1606',
                        userName: 'Ily1606',
                        icon: facebookIcon,
                        name: "Facebook",
                        class: "w-6 text-blue-400 inline-block"
                    },
                    {
                        link: 'https://github.com/Ily-1606',
                        userName: 'Ily-1606',
                        icon: githubIcon,
                        name: "Github",
                        class: "w-6 text-gray-800 inline-block"
                    }
                ]
            }
        }
    }
}
</script>