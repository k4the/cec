<template>
  <div class="cec-select">
      <button type="button" @click="toggleSelect()">{{selected.text}}
        <span class="icon-toggle">
              <i class="link-icon fas" v-bind:class="{ 'fa-chevron-down': !selectOpen, 'fa-chevron-up': selectOpen }"></i>
          </span>
      </button>
      <div v-show="selectOpen" class="cec-select-list">
          <div v-for="item in this.items" :key="item.id" @click="setSelected(item)" class="list-item">
          {{item.text}}
        </div>
      </div>
  </div>
</template>

<script>
import './cecSelect.scss';
export default {
  name: "CecSelect",
  data() {
    return {
      selectOpen: false,
      selected: {
          text: 'Please choose your address',
          id: 0
      },
      items: [
          {
              text: '21 Dummy Drive',
              id: 1
          },
          {
              text: '22 Dummy Drive',
              id: 2
          },
          {
              text: '23 Dummy Drive',
              id: 3
          },
          {
              text: '24 Dummy Drive',
              id: 4
          },
          {
              text: '25 Dummy Drive',
              id: 5
          },
          {
              text: '26 Dummy Drive',
              id: 6
          },
          {
              text: '27 Dummy Drive',
              id: 7
          },
          {
              text: '28 Dummy Drive',
              id: 8
          }
      ]
    };
  },
  methods: {
      toggleSelect() {
        this.selectOpen = !this.selectOpen;
      },

      setSelected(selected) {
          console.log('selected', selected);
        this.selectOpen = false;
        this.selected = selected;
        // const item = {
        //     data: selected,
        //     label: this.label
        // };
        //this.singleSelectedItems.emit(item);
    }
  }
};
</script>
<style lang="scss">
</style>