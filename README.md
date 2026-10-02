An AI tool that uses ADB to randomly check your phone screen and remind you to study.
一款通过 ADB 随机检查手机屏幕并提醒你学习的 AI 工具。

📌 Functions / 功能
English	中文
Randomly capture screenshots via ADB.	通过 ADB 随机截取手机屏幕。
Use AI to judge whether you are studying or playing games.	使用 AI 判断你是在学习还是在玩游戏。
Support HTTP chat.	支持 HTTP 在线聊天。
❓ How It Works / 工作原理
Step	English	中文
1	Set up ADB and connect your phone to your computer via USB or Wi-Fi debugging.	配置 ADB，并通过 USB 或无线调试将手机连接到电脑。
2	Fill in the config fields in app.py (OCR path and API key).	在 app.py 中填写配置项（OCR 路径与 API 密钥）。
3	Run app.py.	运行 app.py。
4	Done. Now you can chat online and manage your screen time.	完成。现在你可以在线聊天并管理你的屏幕使用时间。
🛠 Requirements / 环境要求
Dependency / 依赖	Description / 说明
Python 3.x	运行主程序 / Runs the main program
ADB	Android Debug Bridge，用于控制手机 / Android Debug Bridge, controls the phone
Offline OCR	从截图中读取文字 / Reads text from screenshots
API Key	调用 AI 模型 / Calls the AI model
Computer & Target Phone	一台电脑与一台目标手机 / A computer and a target phone
🚀 Quick Start / 快速开始
1. Clone the repository / 克隆仓库
bash
git clone https://github.com/xingdanyun0519-collab/p.git
cd p
2. Set up virtual environment & install dependencies / 创建虚拟环境并安装依赖
bash
python -m venv .venv
.venv\Scripts\pip install -r requirements.txt
Note / 提示：Windows 用户使用上面的命令；Linux / macOS 用户请将 .venv\Scripts\ 替换为 .venv/bin/。
Windows users use the command above; Linux / macOS users should replace .venv\Scripts\ with .venv/bin/.

3. Configure settings in app.py / 在 app.py 中配置
Field / 配置项	Description / 说明
OCR_EXE_PATH	Path to your offline OCR tool (e.g., Umi-OCR) / 离线 OCR 工具的路径（例如 Umi-OCR）
DEEPSEEK_API_KEY	Your API key / 你的 API 密钥
4. Run / 运行
bash
.venv\Scripts\python app.py
📁 Project Structure / 项目结构
text
├── app.py              # Main program / 主程序
├── web/                # Web frontend / 网页前端
│   ├── index.html
│   ├── app.js
│   └── style.css
├── requirements.txt    # Python dependencies / Python 依赖
├── chat.json           # Chat history / 聊天记录
├── history.json        # Screenshot history / 截图历史
└── ui.xml              # UI config / 界面配置
📝 Notes / 注意事项
#	English	中文
1	OCR only captures text from the screen. It does not record images.	OCR 仅提取屏幕上的文字，不会保存图像。
2	When you change OCR tools, update OCR_COMMAND near the top of app.py.	更换 OCR 工具时，请更新 app.py 顶部的 OCR_COMMAND。
3	To force-close apps, edit NON_STUDY_PACKAGES in app.py.	如需强制关闭应用，请修改 app.py 中的 NON_STUDY_PACKAGES。
4	This project sends OCR text and chat history to the AI API. Avoid putting private content into chats if you do not want it processed remotely.	本项目会将 OCR 文本与聊天记录发送至 AI API。如不希望内容被远程处理，请勿在聊天中输入隐私信息。
5	For personal study only.	仅供个人学习使用。
📄 License / 许可
For personal study only. / 仅供个人学习使用。
