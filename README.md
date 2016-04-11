# EmptyLayout

###空页面|错误页面|加载中页面处理

## EmptyLayout使用 ##

1.在布局文件里增加

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
2.代码里增加：

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