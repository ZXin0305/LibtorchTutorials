# LibtorchTutorials

## 前言
本教程旨在教读者如何用c++写模型，训练模型，根据模型预测对象。为便于教学和使用，本文的c++模型均使用libtorch（或者pytorch c++ api）完成搭建和训练等。目前，国内各大平台似乎没有pytorch在c++上api的完整教学，也没有基于c++开发的完整的深度学习开源模型。可能原因很多：
1. c/c++的深度学习已经足够底层和落地，商用价值较高，开发难度偏大，一般不会开源；
2. 基于python训练，libtorch预测的部署形式足够满足大多数项目的需求，如非产品级应用，不会有人愿意研究如何用c++从头搭建模型，实现模型训练功能；
3. Tensorflow的市场份额，尤其时工业应用的部署下市场占比足够高，导致基于libtorch的开发和部署占比很小，所以未见开源。

既然如此，笔者就做这第一人。本教程提供基于libtorch的c++开发的深度学习视觉模型教学，本教程的开发平台基于Windows环境和Visual Sutdio集成开发环境，实现三大深度视觉基本任务：分类，分割和检测。适用人群为：有c++基础，了解面向对象思维，有pytorch编程经验者，对模型落地部署等经验不足者尤为有用。

## 章节安排
本教程分多个章节：
- 第一章：开发环境搭建
- 第二章：张量的常规操作
- 第三章：简单模型搭建
- 第四章：数据加载模块使用
- 第五章：分类模型搭建，训练和预测
- 第六章：分割模型搭建，训练和预测
- 第七章：目标检测模型搭建，训练和预测
- 第八章：总结和使用

在第一章中，笔者将介绍教程使用的开发环境。第二章，笔者将介绍libtorch中的torch::Tensor类的常用操作，便于后续复杂算法的落地实施。第三章，笔者将以一个简单的线性模型为例，介绍如何在c++上创建一个分类或者回归模型。第四章，笔者将介绍如何使用libtorch的dataload模块，这对c++模型的训练极其重要。第五、六、七章中，教程将详细描述如何实现一个c++分类器，一个c++语义分割器，一个c++目标检测器，包含功能分别为：分类图片，语义分割图片，检测图片中的目标。第八章为全部教程的总结和展望。

## 环境搭建
事实上，在前面的[pytorch部署博客](https://allentdan.github.io/2020/12/16/pytorch%E9%83%A8%E7%BD%B2torchscript%E7%AF%87)和[libtorch的QT部署](https://allentdan.github.io/2021/01/21/QT%20Creator%20+%20Opencv4.x%20+%20Libtorch1.7%E9%85%8D%E7%BD%AE/#more)中笔者已经分享了自己搭建libtorch开发环境的记录。其余并无太多要赘述的。