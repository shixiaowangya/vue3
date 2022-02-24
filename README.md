### ref

接受一个内部值并返回一个响应式且可变的 ref 对象。ref 对象仅有一个 .value property，指向该内部值

### toRefs

将响应式对象转换为普通对象，其中结果对象的每个 property 都是指向原始对象相应 property 的 ref.
toRefs 只会为源对象中包含的 property 生成 ref。如果要为特定的 property 创建 ref，则应当使用 toRef.

### reactive

响应式转换是“深层”的——它影响所有嵌套 property.
reactive 将解包所有深层的 refs，同时维持 ref 的响应性.

### 生命周期

beforCreate ===> use setup 初始化前
Create ===> use setup 初始化后
beforMount ===>onBeforMount 挂载前
mount ===> onMount 挂载后
mount ===> onMount 挂载后
beforupdate ===> onBeforupdate 更新前
update ===> onUpdate 更新后
beforDestroy ===> onBeforUnmount 销毁前
destroy ===> onUnmount 销毁后

### activated
被 keep-alive 缓存的组件激活时调用。该钩子在服务器端渲染期间不被调用。
activated --->onActivated
### deactivated
被 keep-alive 缓存的组件失活时调用。该钩子在服务器端渲染期间不被调用。
deactivated ---->onDeactivated

### errorCaptured
在捕获一个来自后代组件的错误时被调用。此钩子会收到三个参数：错误对象、发生错误的组件实例以及一个包含错误来源信息的字符串。此钩子可以返回 false 以阻止该错误继续向上传播。
errorCaptured ---->onErrorCaptured

### vue3 added （新增） 生命周期
renderTracked ----> onRenderTracked
renderTriggered -----> onRenderTriggered

### v3生命周期选项和组合式api之间的映射

![生命周期](C:\Users\wanggaoxian\Desktop\生命周期.png)
