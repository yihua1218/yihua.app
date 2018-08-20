<template lang="pug">
  v-data-table.elevation-1(:headers='headers', :items='desserts', hide-actions='')
    template(slot='items', slot-scope='props')
      td {{ props.item.category }}
      td {{ props.item.name }}
      td {{ props.item.type }}
</template>

<script>
  export default {
    data () {
      return {
        headers: [
          {
            text: 'Category',
            align: 'left',
            value: 'class'
          },
          {
            text: 'Name',
            align: 'left',
            value: 'name'
          },
          {
            text: 'Type',
            align: 'left',
            value: 'type'
          }
        ],
        desserts: [
          {
            category: 'Task',
            name: 'License server, devices and licenses populate',
            type: 'bash',
          }
        ]
      }
    }
  }
</script>