import matplotlib.pyplot as plt
import seaborn as sns

# 设定图形样式
sns.set(style="whitegrid")

# 建立数据
data = {'强化思政融入': 20, '实践教学推进': 15, '拓展学术视野': 30, '微课教学发展': 25}

# 创建一个figure和axes的实例
fig, ax = plt.subplots()

# 生成条形图
bars = plt.bar(data.keys(), data.values(), color='skyblue')

# 在每个条形上添加数值标签
for bar in bars:
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, yval + 1, yval, ha='center', va='bottom')

# 添加标题和坐标轴标签
plt.title('五年课程建设计划')
plt.xlabel('计划')
plt.ylabel('重要度')

# 展示图形
plt.show()


