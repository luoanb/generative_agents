要首先设置一个虚拟环境，您可以按照以下步骤进行：

### 使用 `venv` 模块（Python 3.3 及更高版本内置）

1. **打开命令行窗口**：
   在 Windows 上，您可以打开命令提示符或 PowerShell。在 macOS 或 Linux 上，您可以打开终端。

2. **导航到项目目录**：
   使用`cd`命令（在 Windows、macOS 和 Linux 上都一样）导航到您的项目所在的目录。例如，如果您的项目在名为`myproject`的文件夹中，您可以这样做：

   ```bash
   cd path/to/myproject
   ```

3. **创建虚拟环境**：
   使用 Python 的`venv`模块创建一个新的虚拟环境。假设您希望虚拟环境的名字是`myenv`，您可以运行：

   ```bash
   python3 -m venv myenv
   ```

   这将在当前目录下创建一个名为`myenv`的新文件夹，其中包含了一个隔离的 Python 环境。

4. **激活虚拟环境**：

   - 在**Windows**上：
     ```bash
     myenv\Scripts\activate
     ```
   - 在**macOS 和 Linux**上：
     ```bash
     source myenv/bin/activate
     ```
     激活虚拟环境后，您会在命令行提示符前看到`(myenv)`，表明您现在正在该虚拟环境中工作。

5. **安装依赖**：
   一旦虚拟环境被激活，您就可以安全地安装项目所需的依赖，而不会影响到系统级别的 Python 安装或其他项目。使用`pip`安装`requirements.txt`中列出的依赖：
   ```bash
   pip install -r requirements.txt
   ```

### 使用 `conda`（如果您安装了 Anaconda 或 Miniconda）

如果您安装了 Anaconda 或 Miniconda，您也可以使用`conda`来创建虚拟环境：

1. **打开命令行窗口**。
2. **创建虚拟环境**：
   ```bash
   conda create -n myenv python=3.9  # 这里的3.9可以替换为您需要的Python版本
   ```
3. **激活虚拟环境**：
   - 在**Windows**上：
     ```bash
     conda activate myenv
     ```
   - 在**macOS 和 Linux**上：
     ```bash
     source activate myenv
     ```
4. **安装依赖**：
   同样，激活虚拟环境后，您可以使用`pip`或`conda`来安装依赖。

确保在激活虚拟环境后再安装依赖，这样依赖就会安装到虚拟环境中，而不是全局 Python 环境中。完成项目后，您可以使用`deactivate`命令退出虚拟环境。
