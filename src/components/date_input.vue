/**
 * https://bootstrap-vue.js.org/docs/components/form-input/
 * https://stackoverflow.com/questions/52887744/vue-data-binding-for-b-input-in-b-table-using-bootstrap-vue
 **/
<script>
    export default {
      name: "DateInput",
      props: [ "FieldID", "aDate"],
      methods: {
        sndDateInput: function($event) {
          this.$emit("rcvDateInput", $event.target.id, $event.target.value);
        }
      }
    }
</script>

<template>
    <div class="col-sm-12">
    <b-form-group>
      <label>Start Date</label>
        <span class="input-group-addon rounded-bg">
          <b-form-input type="date" :value="aDate" :id="FieldID" v-on:input="sndDateInput"></b-form-input>
        </span>
        The Date = {{aDate}} {{FieldID}}
    </b-form-group>
    </div>
</template>


