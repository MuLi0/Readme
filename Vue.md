# Vue
## Vue基础
1. data函数返回对象 提供数据
2. 指令 v-bind : v-for v-if v-show v-on @
3. computed对象 缓存 简单操作
4. methods对象 每一次都重新执行 复杂操作、事件监听，公共业务逻辑
5. watch对象
6. 单向绑定 :value 双向绑定 v-model 表单控件事件处理，表单提交事件处理，事件修饰符
7. 可以开发企业官网，app登录页面，旅游网站，内容网站

## Vue进阶
1. v-html v-once
2. 给v-bind v-on绑定动态参数 :[ ]
3. v-for key
4. template
5. 事件传参和多事件处理函数 $event访问和传递原生dom e
6. 事件相关修饰符 如.prevent,.stop,.capture,.self,.once
7. 键盘，鼠标事件的修饰符 如@keyup.ctrl,.alt,.shift.exact,@mouse.down,.right
8. 表单相关修饰符，.lazy,.number,.trim
9. 通过Vue实例访问和修改应用的配置
10. 生命周期钩子函数 

## Vue组件和脚手架
1. 如何创建组件？app.component((),{})
2. 全局注册组件 注册到app上
3. 局部注册组件 导出，导入并添加component组件
4. 脚手架 SFC单一文件组件 Vite/Vue CLi
5. 使用Vite npm init vite@latest /npm install /npm run dev
6. 创建并使用单一文件组件 import导入并添加配置项即可使用
7. props属性 自定义组件内容 通过props传递字符串
8. 组件动态属性值绑定 在app.vue创建对象 然后v-for 加v:bind=""
9. props属性类型验证和默认值 类型验证和值验证，设置默认值
10. 传递组件未定义的props 一般传类修改样式
11. 插槽 slot 传递模板到子组件
12. 使用多个插槽占位 v-slot:name 
13. emit 子组件事件：向父组件传递数据的途径

## 组件深入
1. 响应式props和组件刷新，父组件改变，子组件刷新，子组件不能直接修改父组件属性
2. 使用watch监听props变化
3. 组件数据的流向设计：属性向下，事件向上 props/emit 
4. 组件生命周期和生命周期钩子函数相似
5. 给深层组件中传递属性，provide函数配置项，inject属性
6. 在传递的slot模板中，访问子组件的属性,子组件slot绑定属性值 父组件v-slot接收
7. 样式 app.vue全局样式 scoped 组件局部样式 qpp.vue全局导入，一般为重置和兼容 css module less,scss,postcss
8. 修改scoped的子组件的样式，：deep，：sloted
9. 给样式绑定响应式数据 v-bind()，可以和computed结合
10. 让组件支持v-model指令，在组件的props和emits中分别写入modelValue和update:modelValue
11. 使用多个v-model指令，使用变量名代替modelValue
12. Refs:获取DOM和子组件实例，一般不使用
13. 自定义指令 定义生命周期函数内容 不推荐使用
14. 使用动态组件渲染不同的HTML标签，使用Component :is，还可以渲染不同的组件,数据丢失套<KeepAlive>解决
15. 组件传送，在其它DOM元素挂载组件，使用<teleport to="">, 还可以多次传送
16. 渲染函数 JSX语法，编程式的模板，render函数，使用“指令”。
17. Mixins：组件配置的复用，与组件共同属性的覆盖与合并原则，全局Mixins，给Vue编写插件
18. 异步组件加载：按需加载组件代码，减少文件体积
19. 组件错误处理：全局错误处理，局部错误处理，errorCaptured
    
## 组合式API Compositon API
1. 为什么使用组合式Compostion API而不使用选项式Optional API？区别和优劣
2. 使用setup函数作为Compostion API的入口替代data,methods等选项
3. ref()函数，在setup()函数中定义响应式数据，代替data，响应式数据也叫状态，在setup函数中需要使用.value，在模板中不需要
4. reactive()函数，直接返回响应式数据，只支持对象和数组类型的数据，不需要使用.value，返回的是Proxy对象
5. computed()函数，返回不带参数的回调函数，在回调函数中返回计算后的值，在setup函数中使用需要.value
6. watch()函数，监听ref本身，监听回调函数返回的ref.value，监听对象中基本类型，监听对象类型的响应式熟悉，deep，访问修改前的对象类型响应式数据，子对象，浅拷贝，深拷贝，包括数组
7. 同时监听多个响应式数据，分别监听或监听数组
8. wathcEffect(),接收回调函数，变化再执行
9. wtch()&watchEffect()清理收尾操作，onValidate()
10. 传递和访问Props属性，无法使用this，直接使用props，setup函数的第一个参数
11. 转换非响应性Props为响应性，使用toRefs()
12. ref/reactive创建的数据在Props中的响应性，对象和数组可以保留响应性
13. methods()直接在setup函数中定义函数方法
14. emit自定义事件,setup函数的第二个参数
15. 生命周期钩子
16. Provide和Inject，全为函数，提供和访问响应式数据，使用ref或toRef,reactive
17. 获取template ref
18. 渲染函数：使用context中的slots属性
19. attrs:获取非props属性
20. Composables 最佳组件逻辑复用方式 推荐用use开头
21. script setup defineProps()，Emit()编译器宏无需导入,useSlot(),useAttrs()

## Vue与后台交互
1. HTTP 客户端 请求 包括请求方式 路径与查询参数 HTTP版本 请求头 请求体 服务端 响应 HTTP版本 响应状态码 响应头 响应体
2. Axios