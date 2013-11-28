var NS={}    //设置NS为namespace
/**************************flowplayer相关初始化********************************/
$(function(){
    //播放列表
    var playlist = [{url:"http://www.alo7.com/video/idx/intro.flv"},
                    {url:"http://www.alo7.com/video/idx/film.flv"},
                    {url:"http://www.alo7.com/video/idx/website.flv"},
                    {url:"http://www.alo7.com/video/idx/intro.flv"}
      
      ];
    $f("player", "http://releases.flowplayer.org/swf/flowplayer-3.2.16.swf",{playlist:playlist});   //初始化flowplayer
    var player=$f("player");
    var currentPlay=0;//当前播放的视频序号
 
   
    
    
    

    NS.verticalCenter($(".playerButton"));     //设置playerbutton列表垂直居中

   //playerButtton的hover效果
    $(".playerButton li").hover(function(){
                                  if($(this).parent().hasClass("left")){
                                      $(this).animate({"left":"-=10px"},200);
                                      }
                                   else{
                                       $(this).animate({"left":"+=10px"},200); 
                                       } 
                                  }
                              ,function(){
                                  if($(this).parent().hasClass("left")){
                                      $(this).animate({"left":"+=10px"},100);
                                      }
                                   else{
                                       $(this).animate({"left":"-=10px"},100); 
                                       } 
                                  }
                              ); 
/**   //playerButton 的fade效果
    $(".playerWrap .playerButton").fadeOut(0);
    $("#player").hover(function(){
                               $(".playerWrap .playerButton").fadeIn(200);
                               }
                           ,function(){
                                $(".playerWrap .playerButton").fadeOut(200);
                                }
                           );
     

**/
    
    
   //playerButton功能设置
   $(".prev").click(function(){
                        currentPlay--;
                        if(currentPlay<0){
                            currentPlay=playlist.length-1;
                            }
                        player.play(playlist[currentPlay]);
                        });
                      
   $(".play").click(function(){
                        player.play();
                        });

   $(".pause").click(function(){
                        player.pause();
                        });

   $(".next").click(function(){
                        currentPlay++;
                        if(currentPlay>playlist.length-1){
                            currentPlay=0;
                            }
                        player.play(playlist[currentPlay]);
                        });

   $(".resume").click(function(){
                         player.resume();
                         });

   $(".mute").click(function(){
                         player.mute();
                         });

   $(".screen").click(function(){
                         player.fullscreen();
                         });

   $(".stop").click(function(){
                         player.stop();
                         });
  


   //点播功能
   $(".playList td").each(function(i){
                              $(this).data({"data-video":playlist[i],"number":i});
                              }
                          )
                    .click(function(){
                               player.play($(this).data("number"));
                               currentPlay=$(this).data("number");
                               }
                          );
    });
/***************************************************************************/


//设置jquery对象垂直居中  
NS.verticalCenter=function(elements){
                          var topOffset=-elements.innerHeight()/2;
                          elements.css({top:"50%",marginTop:String(topOffset)+"px"});
                          }

