<template>
  <button :type="nativeType"
          class="or-button"
          :autofocus="autofocus"
          :class="[
            'or-button--'+type,
            buttonSize,
            {
              'is-plain':plain,
              'is-loading':loading,
              'is-round':round,
              'is-circle':circle,
              'is-disabled':disable,
            }
            ]"
          :style="this.$props.disable ? 'cursor: not-allowed;\n':''"
          @click="handleClick"
  >
    <i v-if="loading" class="or-icon-loading"></i>
    <i v-else-if=" icon" :class="icon"></i>
    <span v-if="$slots.default">
      <slot></slot>
    </span>
  </button>
</template>

<script>



export default {
  props:{
    type:{
      default:"default",
      type:String,
    },
    'nativeType':{
      default:'button',
      type:String,
      validator:function (value){
        return ['button','reset','submit'].indexOf(value) !== -1
      }
    },
    autofocus:{
      type:Boolean
    },
    size: {
      type:String,
      validator:function (value){
        return ['medium','small','mini','tiny'].indexOf(value) !== -1
      }
    },
    icon:String,
    plain:Boolean,
    loading:Boolean,
    round:Boolean,
    circle:Boolean,
    disable:Boolean,
  },
  computed:{
    buttonSize:function (){
      if (this.size){
        return 'or-button--'+this.size
      }
      return null
    }
  },
  methods:{
    handleClick:function (event){
      if (this.$props.disable){
        return ;
      }
      this.$emit('click',event)

    }
  }
}

</script>


<style lang="scss" scoped>
  @import "../theme/components/button"
</style>
