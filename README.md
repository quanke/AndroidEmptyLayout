# EmptyLayout

###Android 空页面|错误页面|加载中页面处理，支持所有的布局,使用简单方便

## Screenshots ##
![](/screenshots/data.png)
![](/screenshots/loading.png)
![](/screenshots/error.png)
![](/screenshots/empty.png)
## EmptyLayout使用 ##

> 现在还没有搞定bintray，暂时可以这么使用。

1.把aar/emptylayout-release.aar文件放在libs目录内

2.在app的build.gradle文件添加如下内容

```
repositories {
    flatDir {
        dirs 'libs' //this way we can find the .aar file in libs folder
}
}
```
3、之后在其他项目中添加一句gradle依赖便方便的引用了该library

```
dependencies {
    compile(name:'test', ext:'aar')
}
```

4.在布局文件里增加

```
	<name.quanke.app.libs.emptylayout.EmptyLayout
        android:id="@+id/emptyLayout"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <TextView
            android:id="@+id/textHello"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World!" />

    </name.quanke.app.libs.emptylayout.EmptyLayout>
	
```

5.代码里增加：

```
		findViewById(R.id.btnLoading).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                emptyLayout.showLoading();
            }
        });
        findViewById(R.id.btnEmpty).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                emptyLayout.showEmpty();
            }
        });
        findViewById(R.id.btnError).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                emptyLayout.showError();
            }
        });
        findViewById(R.id.btnData).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                emptyLayout.hide();
            }
        });
```

```
Copyright 2016 ken.cai (http://quanke.name)
 
   Licensed under the Apache License, Version 2.0 (the "License");
 	you may not use this file except in compliance with the License.
   You may obtain a copy of the License at
   http://www.apache.org/licenses/LICENSE-2.0
	Unless required by applicable law or agreed to in writing, software
 	distributed under the License is distributed on an "AS IS" BASIS,
 	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 	See the License for the specific language governing permissions and
 	limitations under the License.
```