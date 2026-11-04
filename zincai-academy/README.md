# ZincAI Academy

面向水系锌离子电池有机正极研究的私人导师课程：从零开始学习 Python、科研数据分析、分子信息学与基础机器学习。授课语言为中文，专业术语附英文名称。每天默认学习 45–60 分钟。

当前课程放在现有 `codex-ppt-skill` 仓库的独立子目录中，方便持续维护。所有命令均从本目录执行；不需要安装原 PPT 项目的依赖。

## 从哪里开始

1. 阅读 [12 周大纲](curriculum/12_week_plan.md)，了解每周目标和项目。
2. 打开 [第一课：Python 是什么？如何帮助锌离子电池研究？](lessons/01_python_intro/README.md)。
3. 运行示例，再自行完成练习；把代码、实际输出和解释发给导师。
4. 反馈后更新 [学习进度](progress.md)，再决定是否进入下一课。

```bash
# 如果当前位于仓库根目录，先进入课程目录。
cd zincai-academy
# 检查 Python，然后运行第一课示例。
python3 --version
python3 lessons/01_python_intro/example.py
# 完成 exercise.py 的 TODO 后，再运行自己的练习。
python3 lessons/01_python_intro/exercise.py
```

如果已经位于 `zincai-academy/`，跳过第一条命令。Windows 终端中若没有 `python3`，可先用 `py --version` 检查，再把以上 `python3` 替换为 `py`。只复制代码框里的命令，不复制终端提示符。

## 环境与依赖

- 课程目标：Python 3.10 或更新版本；本次实际验证环境：Linux x86_64、Python 3.12.14。
- 第一课只用 Python 自带功能，`requirements.txt` 暂无第三方依赖，不需要执行安装命令。
- pandas、matplotlib、RDKit 和 scikit-learn 在相应阶段才安装；到时再提供经过验证的版本与安装说明。
- 先用普通 `.py` 文件完成学习，不要求 Jupyter、Docker、GPU 或付费 API。
- 检查详情见 [环境与验证记录](curriculum/environment.md)。脚本验证通过不等于学习者已经掌握。

## 课程文件

```text
zincai-academy/
├── README.md                    # 项目入口与运行指南
├── AGENTS.md                    # Codex 长期教学规则
├── curriculum/
│   ├── 12_week_plan.md           # 完整大纲与阶段验收
│   ├── lesson_template.md        # 后续教案模板
│   └── environment.md            # 环境和检查记录
├── lessons/
│   └── 01_python_intro/         # 仅展开当前第一课
│       ├── README.md
│       ├── example.py
│       └── exercise.py
├── datasets/
│   ├── README.md                # 数据来源、单位和边界
│   └── simulated/
│       └── lesson01_capacity.csv
├── projects/
│   └── README.md                # 阶段项目任务与验收要求
├── progress.md                  # 掌握证据、问题和下次入口
└── requirements.txt             # 只记录当前实际需要的依赖
```

后续课程按学习表现逐课创建，当前不预写整套课程代码。

## 数据与科研判断

第一课的数据全部为**模拟教学数据（simulated teaching data）**，由导师人为构造，不来自文献或真实电池测试，也不代表任何真实材料。详见 [数据说明](datasets/README.md)。

真实文献数据必须有可核验来源；真实实验数据必须保留实验条件；计算结果必须记录方法；未经验证的科研假设必须单独标记。分子描述符与模型相关性不能直接证明储能机理。

## 每次怎样继续

下次可说：“请读取 ZincAI Academy 的 `AGENTS.md` 和 `progress.md`，继续当前课程。”提交作业时附自己的代码、完整输出或报错、卡住的位置。导师会先检查你的尝试，逐步提示，并用新数据检验理解。

进度记录以实际提交和解释为依据，不以阅读次数或示例运行次数代替掌握情况。仓库按原项目贡献规则通过 PR 审阅变更。
