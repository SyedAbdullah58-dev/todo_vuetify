<template>
  <div class="home pa-10">
    <v-list>
      <v-list-item v-for="item in items" :key="item.id">
        <v-list-item-action>
          <v-checkbox v-model="selectedItems" :value="item.id"></v-checkbox>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>{{ item.name }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>

  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'HomeView',
  data () {
    return {
      items: [
        { id: 1, name: 'Mediation' },
        { id: 2, name: 'Gym' },
        { id: 3, name: 'Develop Payroll Module' },
        { id: 4, name: 'Debug the Module' },
        { id: 5, name: 'pickup kids from school' },
        { id: 6, name: 'Post on LinkedIn' }
      ],
      selectedItems: []
    }
  },
  components: {
  }

}
</script>
