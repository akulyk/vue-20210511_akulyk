<template>
  <button class="btn btn-primary" @click="handleClick">{{ count }}</button>
</template>

<script>
export default {
  props: {
    count: {
      type: Number,
      default: 0,
    },
  },
  model: {
    prop: 'count',
    event: 'increment',
  },
  methods: {
    handleClick() {
      this.$emit('increment', this.count + 1);
    },
  },
};
</script>

<style scoped>
.btn {
  display: inline-block;
  font-weight: 400;
  text-align: center;
  white-space: nowrap;
  vertical-align: middle;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  border: 1px solid transparent;
  padding: .375rem .75rem;
  font-size: 1rem;
  line-height: 1.5;
  border-radius: .25rem;
  transition: color .15s ease-in-out, background-color .15s ease-in-out, border-color .15s ease-in-out, box-shadow .15s ease-in-out;
}

.btn:not(:disabled):not(.disabled) {
  cursor: pointer;
}

.btn-primary {
  color: #fff;
  background-color: #007bff;
  border-color: #007bff;
}
</style>
