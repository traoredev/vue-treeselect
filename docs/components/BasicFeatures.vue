<template>
  <div>
    <treeselect
      :multiple="true"
      :options="options"
      placeholder="Select your favourite(s)..."
      v-model="value"
      />
    <treeselect-value :value="value" />
    <treeselect
      :multiple="true"
      :options="options"
      expand-to-selected-node
      placeholder="Select your favourite(s)..."
      v-model="selected"
      />
    <treeselect-value :value="selected" />
  </div>
</template>

<script>
  export default {
    data: () => ({
      value: [],
      selected: [ 'pear' ],
      options: [ {
        id: 'fruits',
        label: 'Fruits',
        children: [ {
          id: 'apple',
          label: 'Apple 🍎',
          isNew: true,
        }, {
          id: 'grapes',
          label: 'Grapes 🍇',
        }, {
          id: 'bete',
          label: 'bêtes',
        }, {
          id: 'pear',
          label: 'Pear 🍐',
        }, {
          id: 'strawberry',
          label: 'Strawberry 🍓',
        }, {
          id: 'watermelon',
          label: 'Watermelon 🍉',
        } ],
      }, {
        id: 'vegetables',
        label: 'Vegetables',
        children: [ {
          id: 'corn',
          label: 'Corn 🌽',
        }, {
          id: 'carrot',
          label: 'Carrot 🥕',
        }, {
          id: 'eggplant',
          label: 'Eggplant 🍆',
        }, {
          id: 'tomato',
          label: 'Tomato 🍅',
        } ],
      } ],
    }),
  }
</script>
