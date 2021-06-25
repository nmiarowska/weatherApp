<template>
  <div>
      <b-row class="w-80 h-50 m-5 rounded">
        <b-col cols="8" class="bg-light rounded-left p-5">
          <b-row>
            <b-col cols="6" class="px-0 pt-2">
              <b-form-input v-model="text" placeholder="Search for more places" class="border-0"></b-form-input>
            </b-col>
            <b-col cols="3" class="px-0 pt-2">
              <b-form-select v-model="selected" :options="options" placeholder="All places" class="font-weight-bold border-0 ml-4"></b-form-select>
            </b-col>
          </b-row>
          <div class="card border-0 bg-transparent">
          <div class="card-body">
    <p class="fs-1">.fs-1 text</p>
    <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="card-link">Card link</a>
    <a href="#" class="card-link">Another link</a>
  </div>
          </div>    
        </b-col>

        <b-col cols="4" class="bg-dark rounded-right">One of two columns</b-col>
      </b-row>
  </div>
</template>

<script>


export default {
  name: "Home",
  components: {

  },
  data(){
    return{
      selected: null,
      options: [
      { value: null, text: 'All places' },
      { value: 'a', text: 'This is First option' },
      { value: 'b', text: 'Selected Option' },
      { value: { C: '3PO' }, text: 'This is an option with object value' },
      { value: 'd', text: 'This one is disabled', disabled: true }
      ]
    }
  }
};
</script>
