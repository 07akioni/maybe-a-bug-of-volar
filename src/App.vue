<template>
  <NMenu @update:value="handleUpdateMenuValue" :options="menuOptions" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { MenuOption, NCalendar, NMenu } from "naive-ui";
export default defineComponent({
  name: "App",
  components: {
    NCalendar,
    NMenu,
  },
  setup() {
    const menuOptions = [
      {
        label: "Item1",
        key: "item1",
      },
      {
        label: "Item2",
        key: "item2",
      },
    ];

    const handleUpdateMenuValue = (key: string, item: MenuOption) => {
      console.log("key =>", key);
      console.log("item =>", item);
    };

    return {
      menuOptions,
      handleUpdateMenuValue,
    };
  },
});
</script>
