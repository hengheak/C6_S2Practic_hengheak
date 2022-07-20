<template>
  <form action="">
    <div class="card">
    <div class="form-group">
        <input type="text" placeholder="FirstName" v-model="firstName">
    </div>
    <div class="form-group">
        <input type="text" placeholder="LastName" v-model="lastName">
    </div>
    <div class="form-group">
        <input type="text" placeholder="Comment" v-model="comment">
    </div>
    <div class="form-group">
        <Button btnLabel="Add" bgColor="purple" @click="AddFriend" />
    </div>
    </div>
    
  </form>
  <FullCard :FullName="fullName" />
  
</template>

<script>
import Button from './ButtonView.vue';
import FullCard from './CardView.vue';
export default {

    components:{
        Button,
        FullCard
    },
    data(){
        return {
            firstName:"",
            lastName:"",
            comment:"",
            fullName:[],
        }
    },
    methods:{
        AddFriend(e){
            e.preventDefault();
            let data = {};
            data.firstName=this.firstName;
            data.lastName=this.lastName;
            data.comment=this.comment;
            this.fullName.push(data);
            this.firstName="";
            this.lastName="";
            this.comment="";
            console.log(this.fullName)
           

        }
    }

}
</script>

<style>
.card{
    width:15%;
    margin: auto;
    margin-top: 15px;
    padding: 10px;
   box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px, rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px, rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
}
.form-group{
    margin-top:3px;
    padding: 10px;
    box-sizing: border-box;
    
    
}
Button{
    width:92%;
    margin: auto;
    margin-top: 10px;
    padding: 10px;
    color:white;
}

</style>