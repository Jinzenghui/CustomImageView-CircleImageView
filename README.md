# CustomImageView-CircleImageView
这是一个自定义的ImageView，其中函数的执行顺序为：
	<br>　1:setImageDrawable()
	<br>　2:setAdjustViewBounds()
	<br>　3:构造函数：CircleImageView()
	<br>　4:onSizeChanged()
	<br>　5:onDraw()

#Drawable的理解： 
　　<br>  一个Drawable资源是绘图中的一个普通概念，可以在屏幕上绘制出来。在XML资源中通过android:drawable和
android:icon等属性使用它。Drawable资源都是存储在res/drawable目录下的文件，当然，在一个面向对象的语言中，它最终肯定
也会变成一个对象。在Android中，Drawable类代表这类资源。Android中有多种不同类型的drawable。程序中函数setImageDrawable()中调用函数getBitmapFromDrawable()
此处，drawable的类型为BitmapDrawable，所以使用((BitmapDrawable) drawable).getBitmap()返回Bitmap。
　　<br>	这里出现了BitmapDrawable和ColorDrawable。BitmapDrawable是对bitmap的一种包装，可以设置它包装的bitmap在BitmapDrawable
区域内的绘制方式，如平铺填充、拉伸填充或者保持图片原始大小，也可以在BitmapDrawable区域内部使用gravity指定的对齐方式。ColorDrawable
是最简单的Drawable，它实际上是代表了单色可绘制区域，它包装了一种固定的颜色，当ColorDrawable被绘制到画布的时候会使用颜色填充Paint,
在画布上绘制一块单色的区域。
	<br>
	<br>
	<br>BitmapShader是用来做图像渲染的：BitmapShader(Bitmap bitmap, Shader.TileMode tileX, Shader.TileMode tileY)
	<br>bitmap:用来作为填充的位图；<br>tileX:X轴方向上位图的衔接形式；<br>Y轴方向上位图的衔接形式
	<br>
	<br>CLAMP:如果渲染器超出原始边界范围，则会复制边缘颜色对超出范围的区域进行着色；
	<br>REPEAT则是平铺形式重复渲染；
	<br>MIRROR:则是在横向和纵向上以镜像的方式重复渲染位图；


