## 为 layui 扩展的 下拉多选select
在线demo： [http://yelog.org/layui-select-multiple/](http://yelog.org/layui-select-multiple/)

这个在线 demo就是本项目的 `index.html`。 可将项目 `clone` 到本地查看效果。
## 效果图
![效果](http://oncj6b2vl.bkt.clouddn.com/Frg6VGOCjKJ8fdTYkekfsi-Ax9p2.png)

## 参数
| 属性名 | 属性值 | 备注 |
|:-|:-|:-|
| multiple | 无 | 开启多选 |
| lay-search | 无 | 开启搜索 |
| lay-case | 无 | 大小写敏感 |
| lay-omit | 无 | 开启多选简写，显示勾选条数 |
## 使用
1. 将项目中的 `form.js` 覆盖自己项目中的 `form.js`。
2. 引入下面css
```css
select[multiple]+.layui-form-select>.layui-select-title>input.layui-input{ border-bottom: 0}
select[multiple]+.layui-form-select dd{ padding:0;}
select[multiple]+.layui-form-select .layui-form-checkbox[lay-skin=primary]{ margin:0 !important; display:block; line-height:36px !important; position:relative; padding-left:26px;}
select[multiple]+.layui-form-select .layui-form-checkbox[lay-skin=primary] span{line-height:36px !important; float:none;}
select[multiple]+.layui-form-select .layui-form-checkbox[lay-skin=primary] i{ position:absolute; left:10px; top:0; margin-top:9px;}
.multiSelect{ line-height:normal; height:auto; padding:4px 10px; overflow:hidden;min-height:38px; margin-top:-38px; left:0; z-index:99;position:relative;background:none;}
.multiSelect a{ padding:2px 5px; background:#908e8e; border-radius:2px; color:#fff; display:block; line-height:20px; height:20px; margin:2px 5px 2px 0; float:left;}
.multiSelect a span{ float:left;}
.multiSelect a i {float:left;display:block;margin:2px 0 0 2px;border-radius:2px;width:8px;height:8px;padding:4px;position:relative;-webkit-transition:all .3s;transition:all .3s}
.multiSelect a i:before, .multiSelect a i:after {position:absolute;left:8px;top:2px;content:'';height:12px;width:1px;background-color:#fff}
.multiSelect a i:before {-webkit-transform:rotate(45deg);transform:rotate(45deg)}
.multiSelect a i:after {-webkit-transform:rotate(-45deg);transform:rotate(-45deg)}
.multiSelect a i:hover{ background-color:#545556;}
```

## 使用实例
下面实例 开启了下拉多选（`multiple`）, 并开启了检索功能（`lay-search`）。
效果可以参考 在线实例 的 `多选+搜索+大小写不敏感` 模块
```html
<select name="多选+搜索+大小写不敏感" lay-verify="required" multiple lay-search>
    <option value="">请选择您的兴趣爱好</option>
    <option>sing1</option>
    <option selected>sing2</option>
    <option>SING1-大写</option>
    <option>movie1</option>
    <option selected>movie2</option>
    <option>movie3</option>
    <option>MOVIE4</option>
    <option>swim</option>
    <option>moon</option>
</select>
```
> **更多实例参考 在线实例、或 `index.html`。**

## 声明
此项目基于 https://gitee.com/layuicms/XiaLaDuoXuan 项目修改得来，修复了一些bug，扩展了 简化多选、多选搜索、大小写敏感控制等功能。