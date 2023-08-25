<template>
  <the-navigation></the-navigation>
  <main>
    <router-view></router-view>
  </main>
</template>
<script>
  
    import TheNavigation from './components/nav/TheNavigation.vue';
    export default{
      components:{
        TheNavigation,
      },
    data(){
    return{
      teams:[
        {id:'t1',name:'Frontend Engineers',members:['u1','u2']},
        {id:'t2',name:'Backend Engieneers',members:['u1','u2','u3']},
        {id:'t3',name:'Client Consulting',members:['u4','u5']},
      ],
      users:[
        {id:'u1',fullName:'Sdd',role:'Engineer'},
        {id:'u2',fullName:'Dss',role:'Engineer'},
        {id:'u3',fullNmae:'Kss',role:'Engineer'},
        {id:'u4',fullName:'Ssk',role:'Consultant'},
        {id:'u5',fullName:'dtt',role:'Consultant'}
      ],
    };
  },
  provide(){
    return{
      teams:this.teams,
      users:this.users,
    };
  },
};
</script>
<style>
*{
  box-sizing:border-box;
}
html{
  font-family:sans-serif;
}
body{
  margin:0;
}

</style>
