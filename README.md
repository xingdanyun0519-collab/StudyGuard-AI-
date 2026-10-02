StudyGuard AI · Random Screen-Check Study Companion
通过 ADB 随机截取手机屏幕，用 AI 判断你是在学习还是在摸鱼，并提醒你去学习。
Randomly captures your phone screen via ADB, uses AI to tell whether you are studying or slacking off, and reminds you to get back to work.

📌 功能简介 | Features
通过 ADB 随机截取手机屏幕截图。
Randomly capture screenshots via ADB.

使用 AI 判断你是在学习还是在玩游戏。
Use AI to judge whether you are studying or playing games.

支持 HTTP 聊天。
Support HTTP chat.

❓ 工作原理 | How It Works
配置 ADB，通过 USB 或 Wi-Fi 调试连接手机。
Set up ADB and connect your phone to your computer via USB or Wi-Fi debugging.

在 app.py 中填写配置项（OCR 路径与 API Key）。
Fill in the config fields in app.py (OCR path and API key).

运行 app.py。
Run app.py.

完成。现在你可以边聊天边管理自己的屏幕使用时间。
Done. Now you can chat online and manage your screen time.

🛠 环境要求 | Requirements
依赖 Dependency	说明 Description
Python	3.x
ADB	Android Debug Bridge（安卓调试桥）
离线 OCR Offline OCR	从截图中读取文字 / Reads text from screenshots
API Key	调用 AI 模型 / Calls the AI model
一台电脑 + 一台目标手机
A computer and a target phone	用于控制手机 / Controls your phone
🚀 快速开始 | Quick Start
bash
# 1. 克隆仓库 | Clone the repo
git clone https://github.com/xingdanyun0519-collab/p.git
cd p

# 2. 创建虚拟环境并安装依赖 | Set up virtual environment & install dependencies
python -m venv .venv
.venv\Scripts\pip install -r requirements.txt

# 3. 在 app.py 中配置 | Configure settings in app.py
#    OCR_EXE_PATH      -> 你的离线 OCR 工具路径（例如 Umi-OCR）
#                         path to your offline OCR tool (for example Umi-OCR)
#    DEEPSEEK_API_KEY  -> 你的 API 密钥 / your API key
运行 | Run：

bash
.venv\Scripts\python app.py
📁 项目结构 | Project Structure
text
├── app.py              # 主程序 / Main program
├── web/                # Web 前端 / Web frontend
│   ├── index.html
│   ├── app.js
│   └── style.css
├── requirements.txt    # Python 依赖 / Python dependencies
├── chat.json           # 聊天记录 / Chat history
├── history.json        # 截图历史 / Screenshot history
└── ui.xml              # 界面配置 / UI config
📝 注意事项 | Notes
OCR 只提取屏幕上的文字，不会记录图像。
OCR only captures text from the screen. It does not record images.

更换 OCR 工具时，请修改 app.py 顶部的 OCR_COMMAND。
When you change OCR tools, update OCR_COMMAND near the top of app.py.

如需强制关闭应用，请编辑 app.py 中的 NON_STUDY_PACKAGES。
To force-close apps, edit NON_STUDY_PACKAGES in app.py.

本项目会将 OCR 文本与聊天记录发送至 AI API；如果不希望内容被远程处理，请勿在聊天中输入隐私信息。
This project sends OCR text and chat history to the AI API, so avoid putting private content into chats if you do not want it processed remotely.

仅供个人学习使用。
For personal study only.
