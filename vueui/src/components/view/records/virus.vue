<template>
  <vui-group>
    <vui-group-item label="ID:">{{ active_virus.id }}</vui-group-item>
    <vui-group-item label="Description:" v-html="active_virus.description"/>
    <vui-group-item label="Notes:"><view-records-field :editable="(editable & 32) > 0" path="active_virus.notes"><textarea v-model="$root.$data.state.editingvalue"/></view-records-field></vui-group-item>
  </vui-group>
</template>

<script>
export default {
  data() {
    return this.$root.$data.state
  }
}
</script>
