<template>
<div>
    <h3>{{title}}</h3>
    <nav>
        <ul>
            <li v-for="(item, index) in items" :key="index">
                <a :href="item.src">{{item.text}}</a>
            </li>
        </ul>
    </nav>

</div>
</template>

<script>
export default {
        name: "FooterMenu",
        props:{
            title:String,
            items:String
        } 
    }
</script>

<style scoped lang="scss">
@import "../../assets/variables.scss";
h3{
    color:$colorWhite;
    margin-top: 10px;
}
 nav{ 
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: space-between;
    ul{
        
        li{
            list-style: none;
            margin-right: 20px;
           

        a{
            text-decoration: none;
            color: gray;
            text-transform: capitalize;
            font-size: 12px;
        }
        }
    }
}
</style>