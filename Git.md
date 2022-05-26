# Git

**分布式版本控制工具**  vs  集中式版本控制工具

<hr width="300px" style="height: 1px;background-color:grey; "/>


### 集中式版本控制
**同时只能一个人修改代码   &   中央服务器单点故障问题，无法提交更新和协同工作**

<hr width="300px" style="height: 1px;background-color:grey; "/>


### 分布式版本控制工具
**版本控制实在本地磁盘进行，每个客户端都是完整的项目**

<hr style="height: 3px;background-color:grey; "/>


### 工作区  暂存区  本地库

工作区   —git add→    暂存区  —git commit→  本地库
  ↑                                    ↑                                         ↑
写代码                         临时存储                           历史版本

<hr width="300px" style="height: 1px;background-color:grey; "/>

#### 初始化本地库

**进入以后要写代码的目录库，使用 git init 初始化此目录**
**初始化完成后将生成一个，新的初始化的  .git目录（如果在初始化本目录之前，此目录下有其他的文件/目录，这些目录不会被添加到==暂存区==，都在==工作区==**

<hr width="300px" style="height: 1px;background-color:grey; "/>


#### 工作区
**所有在本地库中新建的文件都属于工作区的文件**

<hr width="300px" style="height: 1px;background-color:grey; "/>

#### 暂存区
→ 提交本地库
→删除暂存区文件
**本地库**中所有**没有添加暂存区的文件**都**属于在工作区**
所有在**工作区的文件**都可以使用  **git  add** 命令将工作区的文件**提交到本地库**
**提交到暂存区中**可以使用 **git rm cached filename**命令**将暂存区的文件删除（工作区的文件(源文件)不会被删除）**

<hr width="300px" style="height: 1px;background-color:grey; "/>


#### 本地库
→git reset --hard 版本号 （切换版本）
添加暂存区之后，不会产生新的版本，还需要提交本地库，才能产生新的版本信息
添加本地库之后，git会记录此版本下所有文件的信息，当返回此版本的时候只会显示提交的时候提交的所有文件和对应的内容

<hr style="height: 3px;background-color:grey; "/>

### 分支

==切换分支的时候必须每一个文件都提交到此分支的本地库，否则error==
branch
**git branch**  BRANCH_NAME  **创建分支**
git branch -v
**git checkout**   BRANCH_NAME   **选择分支**
**git merge**   BRANCH_NAME    **合并分支**

<hr width="300px" style="height: 1px;background-color:grey; "/>

#### 分支合并

<hr width="300px" style="height: 1px;background-color:grey; "/>

#### 冲突合并
（master|MERGING）
**冲突合并的时候需要自行打开冲突的文件，由用户决定要留下那些东西**
**修改完毕之后添加到暂存区，并且提交到本地库，此时产生新的版本信息**
**==提交到本地库的时候不能再写文件名==**

<hr style="height: 3px;background-color:grey; "/>


