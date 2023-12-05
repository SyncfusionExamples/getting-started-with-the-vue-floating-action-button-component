<script setup>
import { FabComponent as EjsFab } from "@syncfusion/ej2-vue-buttons";
import { ListViewComponent as EjsListview } from '@syncfusion/ej2-vue-lists';
import { ref } from 'vue';
const listObj = ref(null);
const data = [
    { text: 'Hennessey Venom', id: 'list-01' },
    { text: 'Bugatti Chiron', id: 'list-02' },
    { text: 'Bugatti Veyron Super Sport', id: 'list-03' },
    { text: 'SSC Ultimate Aero', id: 'list-04' },
    { text: 'Koenigsegg CCR', id: 'list-05' },
    { text: 'McLaren F1', id: 'list-06' },
    { text: 'Aston Martin One- 77', id: 'list-07' },
    { text: 'Jaguar XJ220', id: 'list-08' },
    { text: 'McLaren P1', id: 'list-09' },
    { text: 'Ferrari LaFerrari', id: 'list-10' },
  ];
  const onButtonClick = function(args)
  {
    const newItem = [{ text: 'Robert', id: 'list-11'}];
    listObj.value.addItem(newItem);
  }
</script>

<template>
   <ejs-fab content="Add" target="#target_list" v-on:click.native="onButtonClick"
                          iconCss="e-icons e-plus" iconPosition="Right"
                          position="TopRight" cssClass="e-outline"></ejs-fab>
   <ejs-listview ref="listObj" id="target_list" :dataSource='data' width="250px" showHeader="true" 
                 headerTitle="Contacts"></ejs-listview>
</template>

<style>
  @import "../node_modules/@syncfusion/ej2-base/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-vue-buttons/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-vue-lists/styles/material.css";
.e-listview {
   border: 1px solid lightgray;
}
</style>
