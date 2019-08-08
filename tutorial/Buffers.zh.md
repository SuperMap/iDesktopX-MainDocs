---
title: 缓冲区分析
---

　　大数据分布式分析支持缓冲区分析，缓冲区分析是根据指定的距离，在点、线、面几何对象周围建立一定宽度的区域的分析方法。缓冲区分析的详细介绍及原理请参见[缓冲区分析原理](../../docs/DataAnalyst/BufferTheory.html)。

　　缓冲区分析在GIS空间分析中经常用到，且往往结合叠加分析来共同解决实际问题。缓冲区分析在农业、城市规划、生态保护、防洪抗灾、军事、地质、环境等诸多领域都有应用。例如，在环境治理时，常在污染的河流周围划出一定宽度的范围表示受到污染的区域；又如扩建道路时，可根据道路扩宽宽度对道路创建缓冲区，然后将缓冲区图层与建筑图层叠加，通过叠加分析查找落入缓冲区而需要被拆除的建筑，等等。

##### 　　功能入口

　　提供了两个功能入口，如下所述：

- 在“在线”选项卡的“分析”组中，选择“缓冲区分析”，即可弹出**缓冲区分析**的参数设置对话框。
- 在**工具箱**，双击“在线分析”中的“缓冲区分析”，或者选中对应功能，将其拖拽到“可视化建模”窗口中，双击即可弹出**参数设置**面板。

##### 　　参数说明

　　缓冲区分析的参数设置分为登录iServer、源数据、分析参数三个部分，前两部分的操作说明请参见[数据输入](DataInputType.html)页面，分析参数的介绍如下：

1. **分析范围**：选填参数，当不设置时，默认为输入数据集的全幅范围，范围分析的输入顺序为左下右上，中间以英文的逗号隔开，例如：-74.050,40.650,-73.850,40.850。除了手动输入范围外，还可以通过复制属性中的数据集或对象范围，将其粘贴至此，粘贴后将左下右上等字符删除即可。
2. **缓冲距离**：若未设置缓冲距离字段，则以该参数进行分析，默认值为10。
3. **缓冲距离字段**：若设置了距离字段，将使用每个对象中该字段对应的值作为缓冲距离，此时设置的缓冲距离无效。
4. **缓冲距离单位**：默认值为米，可通过下拉选项进行设置，提供的单位有：米、千米、码、英尺和英里。
5. **融合字段**：选填参数，根据字段值对缓冲区结果面对象进行融合，支持设置非系统字段。
6. 设置好以上参数之后，单击“**执行**”按钮，分析执行完成之后，会在地图窗口打开直接打开执行结果，并且输出窗口会提示分析结果的存储路径。


