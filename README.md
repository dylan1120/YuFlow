# YuFlow

/n8n-research-bot
│── docker-compose.yml        # Docker 管理 n8n & FastAPI
│── .env                      # 環境變數（AWS Key、Notion Token）
│── README.md                 # 專案說明
│
├── backend/                  # FastAPI 主要後端
│   ├── main.py               # FastAPI 入口（啟動 API）
│   ├── dependencies.py        # 依賴函數（AWS、Notion）
│   │
│   ├── services/              # API 服務（功能模組）
│   │   ├── arxiv_service.py   # arXiv API 搜尋
│   │   ├── notion_service.py  # Notion API 操作
│   │   ├── keyword_extractor.py # 關鍵字提取（AWS AI）
│   │   ├── aws_ai_service.py  # AWS AI 服務（Bedrock / Comprehend）
│   │
│   ├── models/                # 數據結構（Pydantic）
│   │   ├── paper.py           # 論文數據結構
│   │   ├── keyword.py         # 關鍵字數據結構
│   │
│   ├── utils/                 # 工具函數
│   │   ├── pdf_parser.py      # 解析 PDF
│   │   ├── text_cleaner.py    # 清理文本
│   │
│   ├── requirements.txt       # Python 依賴庫
│   ├── Dockerfile             # FastAPI Docker 設定
│
├── notion/                    # Notion 設定
│   ├── database_schema.json    # Notion 資料庫結構
│   ├── notion_template.md      # Notion 紀錄格式
│
├── scripts/                   # 測試腳本
│   ├── test_arxiv.py          # 測試 arXiv API
│   ├── test_notion.py         # 測試 Notion API
│   ├── test_pipeline.py       # 測試整體流程
│
└── logs/                      # 錯誤日誌
