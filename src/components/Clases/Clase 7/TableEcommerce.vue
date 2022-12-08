<template>
    <div  >  
            {{getKeys(objetos[0])}}   
            <table class="table" :style="background_color">
                    <thead>
                        <tr :style="th_color">
                            <th  scope="col" v-for="(objeto, index) in keys" :key="index"> {{objeto}} </th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="(objeto,index) in objetos" :key="index">
                            <td v-for="(k, index) in objeto" :key="index">{{k}}</td>
                        </tr>
                    </tbody>
            </table>
        </div>
</template>
  
<script>

import { misMixin } from '@/mixins/mixinglobal';
export default {
    name: 'ConMixin',
    mixins: [misMixin],
    props: {
        objetos: Array,
        th_color: Object,
        background_color: Object
    },
    data() {
        return {
        keys: [],
        values:[]
    }},
    methods: {
        getKeys(objeto) {
            this.keys = Object.keys(objeto);
        },
        getValues(objeto) {
            this.values = Object.values(objeto);
        }
    },
};

</script>
    <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>