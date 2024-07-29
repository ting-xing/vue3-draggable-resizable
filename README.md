### Vue3DraggableResizable

本项目属于 https://github.com/a7650/vue3-draggable-resizable 下游项目。

#### 额外特性
* 减少打包后体积 🤏
* 可在 Nuxt 里使用 🆕
* 支持 ESM 🆕

#### 新参数
新增 parentScaleX  和 parentScaleY 属性，将css的比例绑定上去可兼容缩放问题。

https://github.com/a7650/vue3-draggable-resizable/issues/74

```css
.parent{
  transform: scaleX(2) scaleY(3);
}
```

```vue
<div class="parent">
  <Vue3DraggableResizable :parent-scale-x="2" :parent-scale-y="3"></Vue3DraggableResizable>  
</div>
```

##### 动态参考线

`adsorbCols` 和 `adsorbRows` 参数支持 Ref 类型值

```ts
const adsorb = ref([10,20,30])
```
```vue
<Vue3DraggableResizable :adsorbCols="adsorb" :adsorbRows="adsorb"></Vue3DraggableResizable>
```
