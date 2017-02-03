# 
简单的实现啦九宫格抽奖的原理

实现原理：


   主要是以setTimeout方法来实现，方法的死循环调用做到的动画效果，得到结果跳出循环
    
 
    1.配置
    
  
               var lucky = {
        
                  endNum : 8,//Math.floor(Math.random()*($("#lucky td").length - 2)+1),  //抽奖结果
                  quan   : 9, //转动多少圈停止
                  timer  : null, //控制器
                  speed  : 30, //转动的速度

                }
     
    2.调速器

                if( currentQuan > (lucky.quan-4)){

					lucky.speed = 40

				}
				if( currentQuan > (lucky.quan-3)){

					lucky.speed = 70

				}
				if( currentQuan > (lucky.quan-2)){

					lucky.speed = 100

				}
				if( currentQuan > (lucky.quan-1)){
					lucky.speed = 120

				}
				if( (currentQuan > (lucky.quan-1)) && Math.abs( currentNum - lucky.endNum ) <= 5){
					lucky.speed = 200

				}
				if( (currentQuan > (lucky.quan-1)) && Math.abs( currentNum - lucky.endNum ) <= 2){
					lucky.speed = 300

				}
        
        
   
 
