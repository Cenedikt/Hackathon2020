<template>
  <div>
    <b-button v-b-toggle.collapse-1 variant="primary">Filter</b-button>

    <b-collapse id="collapse-1" class="mt-2">
      <b-card>

        <div>
          <b-button v-b-toggle.collapse-1-inner size="sm">Art</b-button>
          <b-collapse id="collapse-1-inner" class="mt-2">
            <b-card>
              <b-list-group>
                <b-list-group-item>Sport</b-list-group-item>
                <b-list-group-item active>Theater</b-list-group-item>
                <b-list-group-item>Konzert</b-list-group-item>
                <b-list-group-item>Musseum</b-list-group-item>
                <b-list-group-item>Etc...</b-list-group-item>
                <b-list-group-item>Iwan ist AWESOME</b-list-group-item>
              </b-list-group>
            </b-card>
          </b-collapse>
        </div>

        <div>
          <b-button v-b-toggle.collapse-2-inner size="sm">Datum</b-button>
          <b-collapse id="collapse-2-inner" class="mt-2">
            <b-card>
              <b-container fluid>
                <b-row class="my-1" v-for="type in types" :key="type">
                  <b-col sm="3">
                    <label :for="`type-${type}`">
                      Datum:
                    </label>
                  </b-col>
                  <b-col sm="9">
                    <b-form-input :id="`type-${type}`" :type="type"></b-form-input>
                  </b-col>
                </b-row>
              </b-container>
            </b-card>
          </b-collapse>
        </div>

        <div>
          <b-button v-b-toggle.collapse-3-inner size="sm">Handycap</b-button>
          <b-collapse id="collapse-3-inner" class="mt-2">
            <b-card>
              <b-list-group>
                <b-list-group-item active>
                    Rollstuhlgerecht
                </b-list-group-item>
                <b-list-group-item >
                    Gebärdensprache
                </b-list-group-item>
                <b-list-group-item>
                    Mehrsprachig
                </b-list-group-item>
              </b-list-group>
            </b-card>
          </b-collapse>
        </div>

        <div>
          <b-button>filtern</b-button>
        </div>
      </b-card>
    </b-collapse>
  </div>
</template>

<script>
export default {
  data  () {
    return {
      types: [
        'date'
      ]
    }
  },
  methods: {
    beButton1 () {
    },
    beButton2 () {
    },
    beButton3 () {
    }
  }
}
</script>
