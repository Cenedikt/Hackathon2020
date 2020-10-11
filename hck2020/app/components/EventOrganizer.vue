<template>
  <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group
        id="input-group-1"
        label="Titel:"
        label-for="input-1">
        <b-form-input
          id="input-1"
          v-model="form.title"
          type="text"
          required
          placeholder="Veranstaltungstitel hinzufügen"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Beschreibung:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.description"
          required
          placeholder="Bitte fügen Sie eine Beschreibung hinzu"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label="Veranstaltungstyp:" label-for="input-3">
        <b-form-select
          id="input-3"
          v-model="form.event"
          :options="event"
          required
        ></b-form-select>
      </b-form-group>

      <b-form-group id="input-group-4" label="Max. Teilnehmeranzahl:" label-for="input-4">
        <b-form-input
          id="input-4"
          v-model="form.max"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-5">
        <b-form-checkbox-group v-model="form.checked" id="checkboxes-4">
          <b-form-checkbox value="rollstuhl">Rollstuhlgerecht</b-form-checkbox>
          <b-form-checkbox value="gebaerden">Gebärdensprache</b-form-checkbox>
          <b-form-checkbox value="sprachen">Mehrsprachig</b-form-checkbox>
        </b-form-checkbox-group>
      </b-form-group>

      <b-form-group id="input-group-6">
          <b-form-input
          id="input-5"
          v-model="form.date"
          type="date"
          required
          ></b-form-input>
       </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger">Reset</b-button>
    </b-form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      form: {
        title: '',
        description: '',
        event: null,
        max: 0,
        date: '',
        checked: []
      },
      event: [{ text: 'Select One', value: null }, 'Sport', 'Theater', 'Konzert', 'Musseum', 'Etc...'],
      show: true
    }
  },
  methods: {
    onSubmit (evt) {
      evt.preventDefault()
      alert(JSON.stringify(this.form))
    },
    onReset (evt) {
      evt.preventDefault()
      // Reset our form values
      this.form.email = ''
      this.form.name = ''
      this.form.event = null
      this.form.max = 0
      this.form.date = ''
      this.form.checked = []
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>
