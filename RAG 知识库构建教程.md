
![QQ_1745382399655](https://github.com/user-attachments/assets/5c8c599e-8fec-44bc-99b8-5e6e7ed8b0bb)
- 本页面添加本地的DS模型或者QW模型 
- 连接到主机输入Dokcer ps 命令
  ![image](https://github.com/user-attachments/assets/1fa827ad-3d0a-4c4c-893e-16961684f010)
- 找到对应的ollama容器ID输入 docker exec -it 300466c38b34 /bin/bash 进入容器
- 执行ollama list
  ![image](https://github.com/user-attachments/assets/5cb997fc-846e-46ff-8637-e97276fbe8ad)
- 蓝色为LLM模型 红色为嵌入式模型
- 若无上述模型 访问 https://ollama.com/search?c=embedding 嵌入式模型网站
- 若无上述模型 访问 https://ollama.com/library/deepseek-r1 DS模型网站
- 找到合适的嵌入式模型 ollama pull bge-m3 复制模型下载命令
![image](https://github.com/user-attachments/assets/87e32259-b09e-443a-aad8-63a22dbbb152)
- 选择型号后下载
![QQ_1745383729993](https://github.com/user-attachments/assets/20b458bd-f145-466b-a447-a14705221714)
模型名称通过ollama list 查看
基础ulr 为本机ip地址 或者 ollama 开放的端口地址
选择是嵌入是模型还是LLM模型 添加模型


