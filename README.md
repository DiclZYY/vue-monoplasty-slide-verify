# vue-slide-verify

> A Vue plugin to slide verify [Demo](https://monoplasty.github.io/vue-slide-verify/),forked from [monoplasty/vue-monoplasty-slide-verify](https://github.com/monoplasty/vue-monoplasty-slide-verify)


## install

```shell
npm install --save vue-slide-verify
```

## Usage

```html
<template>
    <slide-verify ref="verifyCode" :l="42" :r="10" :w="310" :h="155" @success="onSuccess" @fail="onFail" @refresh="onRefresh"></slide-verify>
</template>
<script>
import Vue from 'vue';
import SlideVerify from 'vue-slide-verify';
Vue.use(SlideVerify);//use the plugin
export default = {
    //...
    methods:{
        onSuccess(){},
        onFail(){},
        onRefresh(){},
        freshVerify(){
            //refresh slide-verify manually.
            this.$refs['verifyCode'].refresh();
        }
    }
    //...
}
</script>
```

## Document

### Props

|    Param    |  Type  |                                   Describe                                    |
| :---------: | :----: | :---------------------------------------------------------------------------: |
|      l      | Number |                                 block length                                  |
|      r      | Number |                              block circle radius                              |
|      w      | Number |                                 canvas width                                  |
|      h      | Number |                                 canvas height                                 |
|    text     | String |                the tips,default value is 'slide filled right'                 |
| successText | String |    tips after verifing successfully,defaut value is 'verify successfully'     |
|  retryText  | String |            tips after verifing defeat,defaut value is 'try again'             |
|   imgUrl    | String | the url fetching img,default value is 'https://picsum.photos/300/150/?image=' |

### Events

|  Event  |   Type   |        Describe         |
| :-----: | :------: | :---------------------: |
| success | Function |    success callback     |
|  fail   | Function |      fail callback      |
| refresh | Function | refresh button callback |

