# listview-stroke
##listview添加边框不显示

很多人在写listview，使用style文件xxx.xml
<!--0-->
	<shape xmlns:android="http://schemas.android.com/apk/res/android">
    <solid android:color="@color/leftlist_item_normal"/>
    <stroke android:width="1dp" android:color="@color/split_line"/>
  	</shape>
在listview中添加`android:background="@drawable/xxx"`这样的形式添加边框的时候会发现有item的行边框并没有正常显示。


这个问题是由于item在设置了`android:width="match_parent"`属性的时候，item会将整行填满从而将边框遮盖住。
解决的方法就是在listview中加上一行`android:padding="1dp"`的属性，似的显示的内容正好留出边框大小的位置，这样就不会发生遮盖的问题了。


PS:**这个比较简单我就不贴代码了**
