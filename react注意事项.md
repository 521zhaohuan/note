# react数据渲染
当在一个函数里改变state状态值时，而另一个函数恰好要用到这个state状态值，那么一定要传值给该函数，
因为state没有走render函数，不会自动更新，所以需要传值给相应的函数，拿到最新的数据才行

# Form表单

antd组件里边form表单的包裹写法正常为

```
export default connect((state) => {

return {

   data: state.registerAppoint,

   cache: state.cache

  };
})(Form.create()(RegisterAppoint));
```



```j
如果子组件向父组件通过`<view ref={form => props.handleForm} />`传值时出现错误可以换一种写法，将form.create包裹在外侧。

```
  esg：

```
export default Form.create()(connect((state) => {

return {

   data: state.registerAppoint,

   cache: state.cache

  };
})(RegisterAppoint));





```