<template>
  <div>
    <label class="label">{{ field.title }}</label>
    <div class="control">
      <input
        type="text"
        class="input"
        :name="field.name"
        v-model="data[field.name]"
        :placeholder="field.title + ' giriniz'"
        :disabled="field.disabled"
        :readonly="field.readonly"
      />
    </div>
    <p class="help" v-if="field.note">{{ field.note }}</p>
  </div>
</template>

<script>
export default {
  props: ["field", "data"]
};
</script>