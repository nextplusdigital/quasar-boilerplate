<template>
  <app-crud-form v-bind="$props"></app-crud-form>
</template>

<script type="text/javascript">
  import AppCrudForm from 'genesis/components/crud/Form.vue'

  export default {
    name: 'crud-form',
    components: {
      AppCrudForm
    },
    props: {
      scopes: {
        type: Object,
        default: () => ({
          index: {},
          create: {
            method: 'create'
          },
          edit: {
            method: 'update'
          },
          view: {
            readonly: true
          }
        })
      },
      service: {
        type: Object,
        required: true,
        default: () => ({})
      },
      path: {
        type: String,
        required: true,
        default: () => ''
      },
      schemas: {
        type: Array,
        required: true,
        default: () => ([])
      },
      actions: {
        default: () => null
      },
      component: {
        type: String,
        default: () => 'field'
      },
      id: {
        type: String,
        default: () => 'id'
      },
      bottom: {
        type: Boolean,
        default: () => true
      },
      top: {
        type: Boolean,
        default: () => true
      },
      floating: {
        type: Boolean,
        default: () => true
      },
      timeout: {
        type: Number,
        default: () => 100
      },
      debug: {
        type: Boolean,
        default: () => false
      },

      rule: {
        type: String,
        default: () => ''
      },
      separator: {
        type: String,
        default: () => ''
      },
      changer: {
        type: String,
        default: () => '~'
      },

      scope: {
        type: String,
        default: () => 'view'
      },
      messages: {
        type: Object,
        default: () => ({
          create: 'Registro criado com sucesso',
          read: '',
          update: 'Registro atualizado com sucesso',
          delete: 'Registro apagado com sucesso'
        })
      },
      handlers: {
        type: Object
      },
      tabs: {
        type: Array,
        default: () => ([])
      },
      tab: {
        type: String,
        default: () => ''
      },
      change: {
        type: Function
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
</style>
