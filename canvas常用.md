#canvas 常用


##形状
>矩型
*ctx.fillRect 		填充矩形   left top width height
*ctx.strokeRect 	框线举行
*Rect(x,y,width,height)
>圆
*ctx.arc()    圆

>线
*ctx.beginPath() 		开始
*ctx.moveTo() 			移动画笔到某点
*ctx.lineTo() 			让路径中拥有(并不会直接绘制)一条到某点的线
*ctx.rect() 			让路径中拥有(并不会直接绘制)一条道某点的线
*ctx.fill() 			填充当前路径
*ctx.stroke() 			描边当前路径
*ctx.closePath() 		结束

清理画布
*1.ctx.clearRect(0,0,600,600);  清理画布
*2.设置宽高  cnavas.width=canvas.height=600;`aw

*ctx.quadraticCurveTo(cp1x,cp1y,cp2x,cp2y,x,y)   二次贝塞尔
*ctx.bezierCurveTo(cp1x,xp1y,xp2x,cp2y,x,y) 	 三次贝塞尔


##样式
线性渐变
*var jianbian=ctx.creatLinearGradient(x1,y1,x2,y2)
jianbian.addColorStop(0.3,'#fff');
径向渐变
*var jianbian=ctx.creatRedialGradientGradient(x1,y1,x2,y2);
jianbian.addColorStop(0.3,'#fff');
*ctx.fillStyle = 'rgba(0,0,0,0)';
*ctx.strokeStyle = '#1b2888';
*ctx.lineCap ='round' ;线的末尾
*ctx.setLineDash([10,3]);

*
*
*

##位移(挪动画布)
只保存画布(包含画笔)‘状态’ 不保存任何图像
*ctx.save()
*ctx.restore() 			
save 和 restore 方法是用来保存和恢复 canvas 状态的
*ctx.translate()  		移动
*ctx.rotate() 			旋转


##画布的编程模式
1.清除
2.重绘

##拿到当前函数
var now = new DatE();
now.getSeconds   当期

#图片填充
1. window.onload = function(){
	var img=..;
	var xxx = ctx.createPattern(img,'no-repeat');
	ctx.fillStyle = xxx;
}
onload  加载完成以后
img.onload =function(){
	ctx.drawImage(this,x,x,width,height)
}



bower install jquery  导jquery