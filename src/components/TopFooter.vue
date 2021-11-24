<template>
<section class="top-footer">
  <div class="container big-logo">

    <div class="lists">

      <div class="left column">
        <ul>
          <li>DC COMICS</li>
          <li v-for="(item, index) in DcComics" :key="index">
            {{item.title}}
          </li>
        </ul>

        <ul>
          <li>SHOP</li>
          <li v-for="(item, index) in Shop" :key="index">
            {{item.title}}
          </li>
        </ul>
      </div>


      <div class="center column">
        <ul>
          <li>DC</li>
          <li v-for="(item, index) in DC" :key="index">
            {{item.title}}
          </li>
        </ul>
      </div>


      <div class="right column">
        <ul>
          <li>SITES</li>
          <li v-for="(item, index) in Sites" :key="index">
            {{item.title}}
          </li>
        </ul>

      </div>
      
    </div>

    

  </div>
</section>
  
</template>

<script>
export default {
   name: "TopFooter",
   data(){
     return{

      DcComics: [

        {
          title:"Characters",
          url: ""
        },
        {
          title:"Comics",
          url: ""
        },
        {
          title:"Movies",
          url: ""
        },
        {
          title:"TV",
          url: ""
        },
        {
          title:"Games",
          url: ""
        },
        {
          title:"Videos",
          url: ""
        },
        {
          title:"News",
          url: ""
        },
      
      ],

      Shop: [
        {
          title:"Shop DC",
          url: ""
        },
        {
          title:"Shop DC Collctibles",
          url: ""
        },
        
      ],

      DC: [
        {
          title:"Terms Of Use",
          url: ""
        },
        {
          title:"Privacy policy(New)",
          url: ""
        },
        {
          title:"Ad Choices",
          url: ""
        },
        {
          title:"Avertising",
          url: ""
        },
        {
          title:"Jobs",
          url: ""
        },
        {
          title:"Subscriptions",
          url: ""
        },
        {
          title:"Talent Workshop",
          url: ""
        },
        {
          title:"CPSC Certificates",
          url: ""
        },
        {
          title:"Ratings",
          url: ""
        },
        {
          title:"Shop Help",
          url: ""
        },
        {
          title:"Contact Us",
          url: ""
        },
      ],

      Sites: [
        {
          title:"DC",
          url: ""
        },
        {
          title:"MAD Magazine",
          url: ""
        },
        {
          title:"DC Kids",
          url: ""
        },
        {
          title:"DC Universe",
          url: ""
        },
        {
          title:"DC Power Visa",
          url: ""
        },
      ]


    }
  }
}
</script>



<style lang="scss">
  @import "../assets/styles/vars.scss";
  @import "../assets/styles/mixins.scss";

  .top-footer {
    background-image: url(../assets/img/footer-bg.jpg);
    height: 300px;

    .container {
      @include center(align);
    }

    .big-logo{
      height: 100%;
      background-image: url(../assets/img/dc-logo-bg.png);
      background-position: right;
      background-repeat: no-repeat;
    }

    .lists {
      display: flex;
      width: 50%;

      .column {
        width: calc(100% / 3);
      }
      

    ul {
      list-style: none;
      color: white;
      margin-bottom: 20px;

      &:last-child {
        margin-bottom: 0;
      }
    }

  li {
    color: gray;
    margin-bottom: 4px;

    &:hover{
      cursor: pointer;
        }
      &:first-child{
        color: white;
        font-weight: bold;
        margin-bottom: 15px;
      }
      }
    }
  }


</style>