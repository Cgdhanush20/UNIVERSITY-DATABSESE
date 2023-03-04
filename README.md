# UNIVERSITY-DATABASE

const mongoose = require('mongoose');
const uri = "mongodb+srv://virumalex:Codeitbro@cluster0.eoylmpv.mongodb.net/?retryWrites=true&w=majority";

mongoose.set('strictQuery',false);

mongoose.connect(url,{
    useNewUrlParser:true
}).then(()=>console.log("Database connected"))

const student_Schema=new mongoose.Schema
({
    name:{
        type:String,
        required:[true,'Nmae required']
    },
    SRN:{
        type:String,
        required:[true,'SRN is must']
    },
    moblie_number:{
        type:Number,
        required:[true,'phone no']
    },
    Branch:{
        type:String,
        default:null    
    },
    email:{
        type:String,
        default:null
    },
    semester:{
        type:Number,
        default:null
    }
})
const faculty_Schema=new mongoose.Schema({
    name:{
        type:String,
        required:[true,'enter the name']
    },
    id:{
        type:String,
        required:[true,'id is must']
    },
    mobile_number:{
        type:Number,
        required:[true,'phone no']
    },
    email:{
        type:String,
        default:null
    },
    associated_branch:{
        type:String,
        required:[true,'Enter the branch']
    }
})
