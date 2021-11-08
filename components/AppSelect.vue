<template>
    <div>
        <label :for="select" class="h4">Which is your favorite {{select}} ?</label>
        
        <select @change="$emit('change',$event.target.value)" 
        :id='select' :name="select" class="form-select p-3">
            <option value="all">---Please select a {{select}} </option>
            <option v-for="option in selectOption" :key="option" :value="option"> {{option}} </option>
        </select>

    </div>
</template>
<script>
export default {
    props:{
        select:{
            type:String,
            default:"cuisine"
        },
        selectOption:{
            type:Array,
            default:()=>['tacos','pizza','dim sum'],
        }
    }
}
</script>
<style lang="scss" scoped>
    
</style>