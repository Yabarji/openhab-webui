<template>
  <f7-button v-bind="config" @click="performAction" />
</template>

<script>
import mixin from '../widget-mixin'
import { actionGroup, actionParams } from '@/assets/definitions/widgets/actions'
import { actionsMixin } from '../widget-actions'

export default {
  mixins: [mixin, actionsMixin],
  widget: {
    name: 'oh-button',
    label: 'Button',
    description: 'A button performing an action on click',
    props: {
      parameterGroups: [
        actionGroup(null, 'Action to perform when the element is clicked')
      ],
      parameters: [
        ...actionParams()
      ]
    }
  }
}
</script>
