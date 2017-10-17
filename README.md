# DataPicker [![](https://jitpack.io/v/xiedong11/DataPicker.svg)](https://jitpack.io/#xiedong11/DataPicker)
支持年月日时分多项选择的时间日期选择控件



## Gradle

``` groovy
In Your Project

allprojects {
		repositories {
			maven { url 'https://jitpack.io' }
		}
	}
	
In Your Module
dependencies {
    compile 'com.github.xiedong11:DataPicker:1.0'
}
```
   ``` groovy 
## Usage

CustomDatePicker publishDatePicker = new CustomDatePicker(MainActivity.this, new CustomDatePicker.ResultHandler() {
                    @Override
                    public void handle(String time) { // 回调接口，获得选中的时间
                        System.out.println(time+"----------");
                    }
                }, publishStart, publishEnd, new CustomDatePicker.CancelResultHandler() {
                    @Override
                    public void handleCancel() {
                    }
                });

                // 初始化日期格式请用：yyyy-MM-dd HH:mm，否则不能正常运行
                publishDatePicker.showSpecificTime(true); // 显示时和分
                publishDatePicker.setIsLoop(true); // 不允许循环滚动
                publishDatePicker.show(publishStart);
```
