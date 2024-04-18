<template>
  <div id="contact">
    <div class="container">
      <div class="row">
        <div class="contact-left">
          <h1 class="sub-title">CONTACT ME</h1>
        </div>
        <div class="contact-right">
          <form @submit.prevent="submitForm">
            <div class="form-field">
              <input v-for="(field, index) in formFields" :key="index" :type="field.type" :name="field.name" :placeholder="field.placeholder" v-model="formData[field.name]" :required="field.required">
            </div>
            <button type="submit" class="btn btn2">Submit</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const formFields = ref([
  { type: 'text', name: 'Name', placeholder: 'Your Name', required: true },
  { type: 'email', name: 'Email', placeholder: 'Your Email', required: true },
  { type: 'textarea', name: 'Message', placeholder: 'Your Message' },
]);

const formData = ref({});

const submitForm = () => {
  console.log('Form data:', formData.value);
  resetForm();
};

const resetForm = () => {
  formData.value = {};
};
</script>
 