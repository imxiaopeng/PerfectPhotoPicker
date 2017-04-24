# PhotoPicker   

forked from liuling (https://github.com/zhaoyun2013/photopicker.git)
An android library to pick photo from gallery

# Sample

###### multi-selection mode

<br/>
###### single-selection mode

<br/>

###### gif
![image](https://raw.githubusercontent.com/liuling07/PhotoPicker/master/sample.gif)
<br/>
# Usage
```
Intent intent = new Intent(MainActivity.this, PhotoPickerActivity.class);//图片选择页面
intent.putExtra(PhotoPickerActivity.EXTRA_SHOW_CAMERA, showCamera);//是否显示相机按钮
intent.putExtra(PhotoPickerActivity.EXTRA_SELECT_MODE, selectedMode);//选择模式：单选 | 多选
intent.putExtra(PhotoPickerActivity.EXTRA_MAX_MUN, maxNum);//多选模式最大选择图片数
startActivityForResult(intent, PICK_PHOTO);
```

```
@Override
protected void onActivityResult(int requestCode, int resultCode, Intent data) {
    super.onActivityResult(requestCode, resultCode, data);
    if(requestCode == PICK_PHOTO){
        if(resultCode == RESULT_OK){
            ArrayList<String> result = data.getStringArrayListExtra(PhotoPickerActivity.KEY_RESULT);//如果模式是单选，集合只有一条记录
           //do what you want to to.
        }
    }
}
```

# License
Copyright 2015 liuling
Edit by 2017 cxp 

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
