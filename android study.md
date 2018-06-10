# android
## inputStream.available()方法
1. 使用场景：在读取文件前，获取可以使用的字节数
2. 使用方法：对于实现的抽象类inputstream的子类，直接调用即可
3. 限制：对于网络应用，由于网络数据发送的延迟等因素，可能存在部分数据未到达本地，导致调用in.available()函数获取的可用数据为0

# 06.11 image and graphics
## drawables
A Drawable is a general abstraction for something that can be drawn.
The various subclasses help with specific image scenarios, and you can extend them to define your own drawable objects that behave in unique ways.

### drawables定义（xml）的方式
#### 首先在res/drawable目录下定义资源:
>
	<?xml version="1.0" encoding="utf-8"?>
	<transition xmlns:android="http://schemas.android.com/apk/res/android" >
    <item android:drawable="@drawable/lamp_off"/>
    <item android:drawable="@drawable/lamp_on"/>
	</transition>
	retrieve and instantiate 定义后重新取回并实例使用

#### 定义布局
drawable定义在ImageView中，另外定义两个button分别用于改变transition状态；另外，Android布局中的 android:onClick=“...”属性设置点击时从上下文中调用指定的方法。该属性值和要调用的方法名称完全一致
>	
	<ImageView
        android:id="@+id/imageview_lamp"
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        android:src="@drawable/res_transition" />
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:onClick="onClick_LampOn"
        android:text="开灯" />
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:onClick="onClick_LampOff"
        android:text="关灯" />


> android的onclick事件
<https://blog.csdn.net/a9529lty/article/details/7542828>


##### 定义布局中出现的问题
1. <item android:drawable="@drawable/lamp_on"/>未在res/drawable-xhdpi目录下添加对应的资源图片文件
2. android:text="关灯" /> 不要直接使用“开灯”,可以在res/strings中定义turn_off
> <https://blog.csdn.net/myoungmeng/article/details/54090891>

##### your project contain err, please fix them
1.eclipse在项目中存在错误时会自动显示出现，但是当项目中已经没有错误了，还是显示此问题，可以通过project clean清楚项目的中的错误信息
> <https://blog.csdn.net/hou09tian/article/details/72356106>

##### 如何使用view的onclick函数
android:onClick
Name of the method in this View's context to invoke when the view is clicked. This name must correspond to a public method that takes exactly one parameter of type View. For instance, if you specify android:onClick="sayHello", you must declare a public void sayHello(View v) method of your context (typically, your Activity).
> <https://developer.android.com/reference/android/view/View.html#attr_android:onClick>
















