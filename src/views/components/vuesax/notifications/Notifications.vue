<template>
 <div>
  <div class="mt-5">
      <h3> Waiting Contract</h3>
    
      <vs-table  search :data="users">
           <template slot="header">
         
        </template>
    <template slot="thead">
      <vs-th sort-key="email">File name</vs-th>
      <vs-th sort-key="id">Date</vs-th>
  
    </template>
    <template slot-scope="{data}">
      <vs-tr :data="tr" :key="indextr" v-for="(tr, indextr) in data">
        <vs-td :data="data[indextr].filename">
          {{ data[indextr].filename }}
        </vs-td>
          <vs-td :data="data[indextr].date">
          {{ data[indextr].date }}
        </vs-td>
         <vs-chip color="#FFB300" >Download</vs-chip>
        

      
      
          
          
          
      </vs-tr>
    </template>
  </vs-table>
   <vs-button  style="margin-left:1150px"  text-color="#ffffff" @click="$router.go(-1)" type="filled">Back</vs-button>
   </div></div>
    
 </template>

 
<script>
export default {
  data() {
    return {
      selected: [],
      'tableList': [
        'vs-th: Component',
        'vs-tr: Component',
        'vs-td: Component',
        'thread: Slot',
        'tbody: Slot',
        'header: Slot'
      ],
      users: [
        {
          "filename": "ProjectA.docx",
          "date": "11/12/2020",
          
        },
       {
          "filename": "ProjectB.docx",
          "date": "12/12/2020",
        }, {
          "filename": "ProjectC.docx",
          "date": "13/12/2020",
        }, {
          "filename": "ProjectE.docx",
          "date": "14/12/2020",
        }, {
           "filename": "ProjectF.docx",
          "date": "15/12/2020",
        },
      ]
    }
  },
}
</script>      
<style>
</style>