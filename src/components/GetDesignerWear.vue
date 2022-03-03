<template>
    <div>
        <p v-for="stud,index in getDesignerWear" :key="index">{{ stud.name }} | {{stud.designer}} </p>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data(){
        return{
            getDesignerWear:[]
        }
    },
    created(){
        axios.get('http://localhost:8084/getdesignerwear').then((resData) =>{
              this.getDesignerWear = resData.data;
        });
    }    
}
</script>

