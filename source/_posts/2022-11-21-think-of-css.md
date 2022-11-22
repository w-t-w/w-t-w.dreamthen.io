---
title: think of css
date: 2022-11-21 20:01:20
tags: [css]
categories: css
---

# css

#### 水平居中

  对于父子关系的布局，如何让子元素居中就是一个课题~

> text-align + inline-block

  ```css
  .parent {
      text-align: center;
  }

  .children {
      display: inline-block;
  }
  ```

> absolute + transform(translate)

  ```css
  .parent {
      position: relative;  
  }

  .children {
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
  }
  ```

> table + margin

  ```css
  .parent {
      display: table;
      margin: 0 auto;
  }
  .children {
  }
  ```

> flex + justify-content

  ```css
  .parent {
      display: flex;
      justify-content: center;
  }
  
  .children {
  }
  ```

#### 垂直居中

> table-cell + vertical-align

  ```css
  .parent {
      display: table-cell;
      vertical-align: middle;
      height: 100px;
  }

  .children {
  }
  ```

> absolute + transform(translate)

  ```css
  .parent {
      position: relative;
      height: 100px;
  }

  .children {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
  }
  ```

> flex + align-items

  ```css
  .parent {
      display: flex;
      align-items: center;
  }

  .children {
  }
  ```

#### 水平垂直居中

> flex

  ```css
  .parent {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .children {
  }
  ```

> absolute + transform(translate)

  ```css
  .parent {
      position: relative;
  }

  .children {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
  }
  ```

#### BFC

> 分类

  - 浮动元素 float,除了 none 以外的情况
  - 定位元素 position(absolute、fixed)
  - display(inline-block、table-caption、table-cell)
  - overflow(auto、hidden、scroll)

> 特性

  - BFC 会形成一个独立的容器,容器内的元素不受容器外元素的影响
  - BFC 的高度计算会联同浮动元素的高度
  - BFC 的区域不会与浮动元素的区域重叠

#### flex

> 分类

  - flex-grow: 设置元素的扩展比例
  - flex-shrink: 设置元素的收缩比例
  - flex-basis: 设置元素的初始值
