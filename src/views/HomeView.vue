<template>
  <div class="home" style="height: 100%; background-color: #eff0f2;">
       <el-row class="header1">
           <div class="content">
                 <el-row>
                       <el-col :span="8" style="height: 50px; display: flex;  align-items: center">
                           <div style="font-size: 11px;color: #909ebb;">Официальный сайт Единой информационной системы в сфере закупок</div>
                       </el-col>
                       <el-col :span="8" style="height: 50px; display: flex;  align-items: center">
                           <div style="font-size: 12px;color: #909ebb;">
                              <i class="el-icon-location"></i><span> мой регион </span> <el-link style="color: blue;">Не выбран <i class="el-icon-caret-bottom"></i></el-link>
                          </div>
                       </el-col>
                       <el-col :span="8" style="height: 50px; display: flex;  align-items: center">
                           <div style="font-size: 14px;color: #909ebb;">
                          
                          </div>
                       </el-col>
                       
                 </el-row>
           </div>
       </el-row>
       <el-divider></el-divider>
       <el-row class="header2">
           <div class="content">
               <el-row>
                    <el-col :span="6">
                      <img alt="Vue logo" src="../assets/logo.jpg" style="height: 100%; width: 100%"> 
                    </el-col>
                    <el-col :span="6" class="" style="height: 100px;">
                        
                    </el-col>
                    <el-col :span="6" class="" style="height: 100px ;display: flex;  align-items: center">
                        <div ><el-link><img src="../assets/mail.svg" class="w3-margin-left"> Техническая поддержка</el-link></div>
                    </el-col>
                    <el-col :span="6" class="" style="height: 100px ;display: flex;  align-items: center">
                        <div ><el-link><img src="../assets/chat.svg" class="w3-margin-left"> Часто задаваемые вопросы</el-link></div>
                    </el-col>
                   
               </el-row>
               
           </div>
           

       </el-row>
       <el-divider></el-divider>
       
        <el-row class="header3 " style="">
          <el-col :span="24" class="">
            <div class="content">
              <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" style="">
            
            <el-menu-item index="1">Все разделы</el-menu-item>
            <el-menu-item index="1-1">Закупки</el-menu-item>
            <el-submenu index="2">
              <template slot="title">Контракты и договоры</template>
              <el-menu-item index="2-1">item one</el-menu-item>
              <el-menu-item index="2-2">item two</el-menu-item>
              <el-menu-item index="2-3">item three</el-menu-item>
            </el-submenu>
            <el-submenu index="3">
              <template slot="title">Планирование</template>
              <el-menu-item index="3-1">item one</el-menu-item>
              <el-menu-item index="3-2">item two</el-menu-item>
              <el-menu-item index="3-3">item three</el-menu-item>
            </el-submenu>
            <el-menu-item index="4">Каталог</el-menu-item>
            <el-submenu index="5">
              <template slot="title">Планирование</template>
              <el-menu-item index="5-1">item one</el-menu-item>
              <el-menu-item index="5-2">item two</el-menu-item>
              <el-menu-item index="5-3">item three</el-menu-item>
            </el-submenu>
            <el-menu-item index="6">Новости</el-menu-item>
            <!-- <el-menu-item index="3" disabled>Info</el-menu-item> -->
          
          </el-menu>
            </div>
          
              </el-col>
        </el-row>
       
       
        <div style=" background-color: #eff0f2;">
          <div class="content" style="margin-top: 40px;">
         <el-row>
             <el-col :span="8" class="w3-padding">
                   <el-card>
                      <el-row>
                          <el-col :span="6"><img src="../assets/to_suppliers.svg" alt=""> </el-col>
                          <el-col :span="6" style="height: 56px ;display: flex;  align-items: center"><span>Поставщикам  </span></el-col>
                      </el-row>
                        
                   </el-card>
            
            </el-col>
             <el-col :span="8" class="w3-padding">
                   <el-card>
                      <el-row>
                          <el-col :span="6"><img src="../assets/to_customers.svg" alt=""> </el-col>
                          <el-col :span="6" style="height: 56px ;display: flex;  align-items: center"><span>Заказчикам  </span></el-col>
                      </el-row>
                        
                   </el-card>
            
            </el-col>
             <el-col :span="8" class="w3-padding">
                   <el-card>
                      <el-row>
                          <el-col :span="6"><img src="../assets/to_control_bodies.svg" alt=""> </el-col>
                          <el-col :span="6" style="height: 56px ;display: flex;  align-items: center"><span>Органам контроля  </span></el-col>
                      </el-row>
                        
                   </el-card>
            
            </el-col>
             
           
         </el-row>        
        </div>
       
        <div class="content" style="margin-top: 40px;">
           <el-row>
                <el-col :span="16" class="w3-padding">
                 
                    <el-carousel trigger="click" style="background-color:white;height: 450px;" class="slideText">
                        <el-carousel-item v-for="(i,index) in slider" :key="index" style="height: 450px;">
                          <div v-if="i.isImg" >
                             <img src="../assets/img3.jpg" alt="" style="width:100%;">
                          </div>
                          <div v-if="!i.isImg" class="" style="padding: 20px;">
                              <el-row>
                                  <el-col :span="8">{{ i.date }}</el-col>
                                  <el-col :span="8"><el-link href="#" class="w3-text-blue">нпа в сфере закупок</el-link></el-col>
                              </el-row>
                             <h1>{{ i.title }}</h1>
                             <p>{{ i.text }}</p>
                          </div>

                          
                          
                          
                        </el-carousel-item>
                      </el-carousel>
               
                  
                </el-col>
                <el-col :span="8" class="w3-padding">
                    <el-card>
                      новости
                    </el-card>
                </el-col>
           </el-row>
        
        </div>
        <div class="content" style="margin-top: 200px;">
           adad


        </div>
        
        </div>
       


  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  data() {
    return {
        activeIndex:'1',
        slider:[
          { isImg:false, title:'Опубликован Федеральный закон от 28.04.2023', date: '28 аперля 2023', text: '', img:''   },
          { isImg:false, title:'Внесены изменения в порядок ведения реестра контрактов, содержащего сведения, составляющие государственную тайну', date: '28 аперля 2023', text: '', img:''   },
          { isImg:true, title:'', date: '28 аперля 2023', text: '', img:'../assets/img3.jpg'   }
        ]
    }
  }
}
</script>
<style>
  .el-divider--horizontal{
    margin: 0;
  }
  .el-divider{
    background-color: #e3eafd;
  }
  .slideText{
      background-image: url('../assets/gerb.png');
      background-size: contain;
      background-repeat: no-repeat;
      background-position: right;
  }
  .el-carousel__button{
     background-color: cadetblue;
  }
</style>