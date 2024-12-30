<template>
    <div 
    :class=" ['fized top-0 right-0 h-[90vh] py-12 px-8 flex flex-col  bg-darkblue text-white transition-all ease-in',
    isOpen ? 'translate-x-0': 'translate-x-full']" 
    @click="toogleBar">

        <FriendProfile 
        image="https://fly.metroimg.com/upload/q_85,w_600/https://uploads.metroimg.com/wp-content/uploads/2023/12/11085444/Gordao-da-XJ.jpg"
        name="Gordin"
        nickname="gordaodaxj"
        />

        <div v-if="isFriend"
        class="text-center">
            <div>
                <a href="">Adiciona em Servidor</a>
            </div>
            <div>
                <a href="#" class="text-red font-bold">Excluir Amigo</a>
            </div>
        </div>
        <div 
        class="text-center"
        v-else>
            <div>
                <a href="#" class="font-bold">Adcionar Amigo</a>
            </div>
        </div>    
    </div>
</template>

<script>
import FriendProfile from '../friends/friendProfile.vue';

    export default {
        name: "RightSidebar",
        data(){
            return{
                isOpen: true,
                isFriend: false
            }
        },
        methods: {
            toogleBar(){
                this.isOpen = !this.isOpen
            }
        },
        components: {
            FriendProfile
        }
    }
</script>