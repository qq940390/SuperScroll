# gzdswSuperScroll
贵州都市网自适应超级滚动滚动jQuery插件
作者： wujinhai (940390@qq.com)
版权： 没有版权，欢迎转载使用。

使用示例：

#html结构
<code><pre>
<div id="marquee">
    <div class="area">
        <ul>
            <li></li>
            <li></li>
        </ul>            
    </div>
    <a href="javascript:;" class="prevbtn">前一个</a>
    <a href="javascript:;" class="nextbtn">下一个</a>
</div>
</pre></code>

#CSS
<style>
#marquee {width:200px;height:50px;overflow:hidden;}
#marquee li{float:left;display:inline;height:50px;}
</style>

#JS
$('#marquee .area').gzdswSuperScroll({timeout:3000, interval:3000, step:1, direction:'left', goleft:'.prevbtn', goright:'.nextbtn'}); //只有一个控制按钮的情况

$('#marquee .area').gzdswSuperScroll({timeout:3000, interval:3000, step:1, direction:'left', goleft:'children .prevbtn', goright:'children .nextbtn'});  //有多个滚动，每个滚动都有控制按钮

#可选参数
{
    timeout:3000,            //等待滚动前的时间，单位为毫秒
    interval:3000,            //滚动间隔时间，单位：毫秒
    autostart:true,         //是否自动开始滚动
    step:1,                    //一次滚动多少像素的步长，或者一次滚动几个子元素
    direction:'left',        //滚动的方向，可选 left  right  up  down
    distance:0,                //一次滚动移动的距离，如果等于0，则按子元素乘以步长滚动
    ismarquee:false,        //是否是连续平滑滚动
    width:0,                //宽度
    height:0,                //高度
    goevent:'click',        //操作按钮的方式
    goleft:'',            //向左或向上滚动的jq选择器
    goright:'',           //向右或向下滚动的jq选择器
    speed:'normal',         //默认的滚动速度，只支持自适应和位移滚动
    easing:''                //jquery easing 效果，默认无效果，使用 easing 效果，一定要确保加载了 jquery.easing 插件
}