## 说明
laydate.js是压缩后的核心代码，laydate.dev.js是开发版的源代码。

need目录存放着核心css

skins是皮肤目录

将laydate pull到你的本地后，将其存放到您js相关目录下的laydate目录，不要改动laydate的结构，否则无法正常运行。

## 愿景
做全球最好的web日期控件。


## 简要
她基于原生JavaScript精心雕琢，兼容了包括IE6在内的所有主流浏览器。她具备优雅的内部代码，良好的性能体验，和完善的皮肤体系，并且完全开源，你可以任意获取开发版源代码，一扫某些传统日期控件的封闭与狭隘。layDate本着资源共享的开发者精神和对网页日历交互无穷的追求，延续了layui一贯的简单与易用。她遵循LGPL协议，您可以免费将她用于任何个人项目。

## 使用方法
一、核心方法：laydate(options);

    options是一个对象，它包含了以下key: '默认值'
    
        elem: '#id', //需显示日期的元素选择器
        
        event: 'click', //触发事件
        
        format: 'YYYY-MM-DD hh:mm:ss', //日期格式
        
        nil:'', //清空及选择时初始值 如：'请选择开始时间'
        
        istime: false, //是否开启时间选择
        
        isclear: true, //是否显示清空
        
        istoday: true, //是否显示今天
        
        issure: true, 是否显示确认
        
        festival: true //是否显示节日
        
        min: '1900-01-01 00:00:00', //最小日期
        
        max: '2099-12-31 23:59:59', //最大日期
        
        start: '2014-6-15 23:00:00',    //开始日期
        
        fixed: false, //是否固定在可视区域
        
        zIndex: 99999999, //css z-index
        
        clear: function(optioins){ //清空回调 传入些插件的配置
        
        },
        
        choose: function(dates){ //选择好日期的回调

        }
        
    
二、其它方法/属性

    laydate.v   //获取laydate版本号
    
    laydate.skin(lib);  //加载皮肤，参数lib为皮肤名 
    
    
    /*
        layer.now支持多类型参数。timestamp可以是前后若干天，也可以是一个时间戳。format为日期格式，为空时则采用默认的“-”分割。
        如laydate.now(-2)将返回前天，laydate.now(3999634079890)将返回2096-09-28
    */
    
    layer.now(timestamp, format);   //该方法提供了丰富的功能，推荐灵活使用。
    
    laydate.reset();    //重设日历控件坐标，一般用于页面dom结构改变时。无参


## 更新日志

1.1

1. layer.now(timestamp,format)支持多类型参数。timestamp支持今天的前若干天，和今天的后若干天，并且如果是一个有效的时间戳,则返回该时间戳对应的日期。如果什么都没传入，则返回当前时间日期。format为日期格式，为空时则采用默认的“-”分割。
2. 优化核心代码。
3. 分和秒的选择改成10列*6行。
4. 修复星期未居中对齐的样式问题
5. 修复在页面加载完毕事件中，调用laydate所造成的立即执行的bug
6. 皮肤包新增[墨绿]。

## 备注
[官网](http://sentsin.com/layui/laydate/)、[Say交流](http://say.sentsin.com/home-58.html)
