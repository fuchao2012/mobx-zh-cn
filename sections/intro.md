# 简介

> 简单, 可扩展的状态管理库

## 概述
MobX是一个通过函数式响应编程使得状态管理更简单，扩展性更强的库。其实MobX的背后理念是非常简单的:

> 应用的状态是本源，其他的部分，都应该从本源派生.

其中包括用户界面，数据序列化，服务器通信等。

React + MobX 是一个非常强大的组合. React提供一个把应用程序的状态渲染成组件树的机制，MobX 提供存储和更新状态然后提供给 React 使用的机制。

React 和 MobX 都提供了一个开发过程中处理问题很理想和独特的的解决方案。React通过虚拟 DOM 减少 UI 渲染过程中 DOM 的操作次数已达到最佳的 UI 渲染。MobX通过一个虚拟的状态依赖图实现只更新 React 组件依赖的状态已达到最佳的的应用状态同步。

## 核心概念
MobX只有几个核心的概念，可以通过下面的实例尝试使用它。[JSFiddle](https://jsfiddle.net/mweststrate/wv3yopo0/)

* 为静态对象添加可观察状态

Mobx 可以通过修饰符的方式，向现有代码添加 `@observable`。即可向其修饰的对象添加观察能力，这里称为“数据源”

* 不使用修复的优雅降级

推荐使用 ES6以上来开发Mobx，当然，你也需要知道如何将其优雅降级，来响应没能正常支持的情况。

```
function Todo() {
 this.id = Math.random()
 extendObservable(this, {
 title: "",
 finished: false
 })
}
```

* 为动态对象添加可计算属性

Mobx 可以通过修饰符的方式，向现有代码添加 `@computed`。通过 setter/getter 的方式实时响应状态的变化，自动计算后会实时响应到视图的变更。

* reactions

## 优点

## 最简实现

## 原则