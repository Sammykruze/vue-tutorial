<template>
    <div>
        <h2>Designer Information</h2>
        <form @submit.prevent="addDesignerWear()">
                <input type="text" placeholder="name" v-model="name"><br>
                <input type="text" placeholder="designer" v-model="designer"><br>
                <input type="text" placeholder="ceo" v-model="ceo"><br>
                
                <button type="submit"> Add Designer</button>
        </form>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data(){
        return{
            name:"",
            designer: "",
            ceo:"",
        }
    },

    methods:{
            addDesignerWear(){
                
                axios.post('http://localhost:8084/adddesignerwear',{
                 name: this.name,
                 designer: this.designer,
                 ceo: this.ceo,
                 }).then((res)=>{
                     console.log(res);
                 })
        }

    }
}
</script>