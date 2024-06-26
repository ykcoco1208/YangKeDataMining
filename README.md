# 数据挖掘作业
### 姓名：杨可  学号:82342218  专业：计算机科学与技术   
## 一、上传文件至GitHub的过程描述   
### 1. 输入已有账号，登录GitHub
![登录](https://github.com/ykcoco1208/YangKeDataMining/assets/97384780/4e62143c-e463-4539-a15f-2359a3965c94)

### 2. 进入个人主页，点击创建新库
![个人主页](https://github.com/ykcoco1208/YangKeDataMining/assets/97384780/c1241068-e265-4a17-96b3-9e66f07b8e81)

### 3. 填写库名称与描述，完成创建
![创建仓库](https://github.com/ykcoco1208/YangKeDataMining/assets/97384780/9855fafe-7be1-430f-bdfa-b733895b68e7)

### 4. 在库的初始化页面点击上传已有文件进入上传页面
![上传文件](https://github.com/ykcoco1208/YangKeDataMining/assets/97384780/225817e2-7081-4105-b5a6-bb4857e47f9a)

### 5. 选择PPT文件并输入本次提交记录的描述，完成文件上传
![选择文件](https://github.com/ykcoco1208/YangKeDataMining/assets/97384780/70262cb2-36ac-4176-a37b-fb2282d68fbf)

## 二、课程学习目标  

我的研究方向为智慧医疗，现阶段所研究的主要内容可以囊括为从医学图像中提取特征并结合网络用于分类。考虑我目前实验推进过程中所欲问题与结合数据挖掘课程中所学知识。我想要学习一种可以用于提取医学图像特征信息的特征提取方法。经过一定的学习与研究，我选中LBP方法，即局部二值模式。
  
### 1、内容介绍  

综合考虑几种局部特征提取方法，如MSER、FAST、LBP等。最终选择LBP算法。  

局部二值模式（Local Binary Patterns，LBP）是一种常用的图像局部特征描述符，用于纹理分析、人脸识别、物体检测等应用中。其基本思想是通过比较像素点与其邻域像素的灰度值，将比较结果编码成二进制数，从而描述图像的局部纹理特征。  

具体来说，对于图像中的每个像素，以其为中心，将其周围的像素灰度值与中心像素灰度值进行比较。如果邻域像素的灰度值大于或等于中心像素的灰度值，则将其标记为1，否则标记为0。这样，针对每个像素，可以得到一个二进制编码。接着，将生成的二进制编码按顺时针或逆时针方向连接起来，形成一个二进制数。最后，将得到的二进制数转换为十进制数，作为该像素点的局部二值模式特征值。  

LBP的主要优点之一是简单高效，计算速度快。由于只涉及局部像素之间的比较，LBP对光照变化和一定程度的噪声具有一定的鲁棒性，能够有效捕获图像的纹理信息。此外，LBP还具有旋转不变性，即对图像进行旋转后，LBP特征不发生改变，这使得其在不同角度下的物体识别具有一定的稳定性。  

LBP也存在一些局限性。首先，LBP只考虑了像素点的局部关系，未能充分利用像素之间的全局空间信息，因此在某些情况下可能会导致特征失真。其次，LBP对图像中的平滑区域和噪声比较敏感，容易受到干扰。另外，LBP生成的特征维度较高，可能需要额外的处理和降维操作，以适应特定的模式识别任务。  

据学习了解，LBP算法具有计算效率高、对光照变化鲁棒性强、局部纹理描述能力强、对部分遮挡具有鲁棒性、简单直观等特点。而在我们采集医学图像作为数据集的过程中，往往收到采集时间、位置的影响，导致数据图像光照不均匀产生差异，对实验准确性造成影响。而医学图像的采集，往往由于人体构造、采集角度与个体差异等原因，其结果存在遮挡影响的可能。通过LBP的学习与应用，亦使得而这些问题得以解决。  

### 2、基本思路  

对于当前实验推进基本思路可概括为以下几点。  

(1) 采集数据集。所采用数据集为自选数据集，体量较小。采集完成亦需对当前数据内容进行筛选，保证数据信息优良。  

(2) 特征融合。结合学习的LBP方法与目前正在使用的特征提取方法，从不同的特征提取方法中收集信息并结合以提高模型性能或表现。  

(3) 数据增强。由于数据集体量较小，在此引入数据增强技术。数据增强可以通过对原始图像进行旋转、缩放、翻转等操作，生成更多样化的训练样本，从而提高模型的泛化能力和鲁棒性。  

(4) 训练模型。选取三种神经网络投入训练，并对比其结果。  

### 3、期望目标
通过学习，可以熟练掌握LBP的基本原理，并加以使用，可以顺利提取图像分类所需特征。并在学习过程中，对特征提取有更进一步的了解，拓宽知识面，开放思维，在之后面对问题时能够有更多的解决思路。
