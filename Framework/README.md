# Framework[![](https://jitpack.io/v/gomoretech/AndroidFramework.svg)](https://jitpack.io/#gomoretech/AndroidFramework)


## 勾芒科技公司安卓项目依赖框架

## 添加说明





### 一、仿iOS的PickerView控件，有时间选择和选项选择并支持一二三级联动效果，支持自定义样式，支持滑动监听

    ——TimePickerView  时间选择器，支持年月日时分，年月日，年月，时分等格式
    ——OptionsPickerView  选项选择器，支持一，二，三级选项选择，并且可以设置是否联动

使用详情具体见: (https://github.com/Bigkoo/Android-PickerView)



### 二、引用比较酷炫的SweetAlertDialog对话框

——Usage

    SweetAlertDialog pDialog = new SweetAlertDialog(this, SweetAlertDialog.PROGRESS_TYPE);
    pDialog.getProgressHelper().setBarColor(Color.parseColor("#A5DC86"));
    pDialog.setTitleText("Loading");
    pDialog.setCancelable(false);
    pDialog.show();

使用详情具体见：(https://github.com/pedant/sweet-alert-dialog)



### 三、新增工具模块

    ——DateUtil: 日期处理工具
    ——StringUtils: 字符串处理工具类
    ——DialogUtils: 提示对话框
    ——ProgressUtils: 加载对话框
    ——TimePickerUtils: 仿IOS模式的时间选择框工具类
    ——MD5Util: MD5加密工具
    ——DensityUtil: 手机屏幕尺寸处理工具
    ——FileTools: 文件读写工具
    ——NetSpeed: 实时网速监测工具
    ——SystemTool: 系统信息工具类



### 四、仿微信底部菜单控件

    ——BottomTabView 仿微信底部菜单，配合ViewPager使用，滑动时颜色渐变



### 五、自定义ViewPager

    ——VerticalViewPager 纵向滑动ViewPager
    ——HorizontalViewPager 横向滑动ViewPager

    FragmentViewPagerAdapter adapter = new FragmentViewPagerAdapter(getSupportFragmentManager(),  new ArrayList<Fragment>());
    viewPager.setAdapter(adapter);
    viewPager.setViewpagerAnimation(HorizontalViewPager.VIEWPAGER_ANIMATION_ZOOMOUT);//设置ViewPager切换动画


### 六、标题栏查询搜索 -> MaterialSearchView

 ——Usage

        布局：

        <FrameLayout
            android:id="@+id/toolbar_container"
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
            <android.support.v7.widget.Toolbar
                android:id="@+id/toolbar"
                android:layout_width="match_parent"
                android:layout_height="?attr/actionBarSize"
                android:background="@color/theme_primary" />
            <com.gomore.gomorelibrary.view.searchview.MaterialSearchView
                android:id="@+id/search_view"
                android:layout_width="match_parent"
                android:layout_height="wrap_content" />
        </FrameLayout>

        代码：

        MaterialSearchView searchView = (MaterialSearchView) findViewById(R.id.search_view);
        	searchView.setOnQueryTextListener(new MaterialSearchView.OnQueryTextListener() {
                    @Override
                    public boolean onQueryTextSubmit(String query) {
                        //Do some magic
                        return false;
                    }
                    @Override
                    public boolean onQueryTextChange(String newText) {
                        //Do some magic
                        return false;
                    }
                });
                searchView.setOnSearchViewListener(new MaterialSearchView.SearchViewListener() {
                    @Override
                    public void onSearchViewShown() {
                        //Do some magic
                    }
                    @Override
                    public void onSearchViewClosed() {
                        //Do some magic
                    }
                });

 使用详情具体见：(https://github.com/MiguelCatalan/MaterialSearchView)


### android studio导入

Step 1. Add the JitPack repository to your build file

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}


Step 2. Add the dependency

    dependencies {
	        compile 'com.github.gomoretech:AndroidFramework:1.2.3'
	}