#eclipse使用经验总结：
1.导入包快捷键： ctrl+shift+o 导入包，使用场景：android开发，mainActivity.java中使用TextView，未导入包的情况下，TextView无法识别，此时可以
	通过快捷键导入包，自动在程序的开始添加import android.widget.TextView;不用自己去查看包名导入
    ctrl+shift+o还可以去除没有使用的包
2.findViewById经常会用到强转类型，可以通过将鼠标移动到findViewById上，然后选择add cast to XX来自动强转