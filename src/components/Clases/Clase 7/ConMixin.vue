<template>
    <div>
        <p>{{fecha}}</p>
        <p>{{fechar}}</p>
    </div>
</template>
  
<script>

import { misMixin } from '@/mixins/mixinglobal';
export default {
    name: 'ConMixin',
    mixins:[misMixin]
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>