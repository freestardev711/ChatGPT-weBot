<h1 align="center">ChatGPT-weBot</h1>



[TOC]

![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/SnapdragonLee/ChatGPT-weBot)

Using ChatGPT-weBot based on ChatGPT(API key call), Stable Diffusion AI drawing and official WeChat hook interface.

<div align="center"> <img src="assets/DALL·E3  - A robot is working hard to transform, modify, and revolutionize the WeChat software.png" width="50%"> </div>



## Support & Features

- [x] Support conversation
- [x] Support context-aware question answering
- [x] Support multithreaded `Stable Diffusion` AI drawing (English Only, Support (Negative) Prompt)
- [x] **Never get banned by using official WeChat execution**
- [x] Support API calls for `gpt-3.5-turbo` and newer models
- [x] Support `WebChatGPT` function
- [x] Support bot's character setting
- [x] Set the keywords to wake up the WeChat robot in private
- [x] Set the keywords to wake up the WeChat robot in the group
- [x] Support replying *at-message* when mentioning your bot in the group
- [x] Get help doc inline
- [x] Regenerate conversation
- [x] Rollback conversation
- [x] Conclusion **(save `token` consumption)**
- [x] Reset the whole conversation
- [x] Support multithreaded conversation in one account
- [x] No need to manually reboot service after error exists
- [ ] Other





## Default configs (Follow steps before you start server)

---> Configurable options [detailed guide](./doc/Config.md)





## Step to Start
0. Environment: Windows 7+， python 3.7+

1. Install all packages listed in `requirements.txt` , use the command like:

   ```bash
   pip install -r ./requirements.txt
   ```

   ***Note that v1.2 requires more packages to be installed and upgraded, so please execute this command once after upgrading.***

   

2. Download package from Github Releases. (You can download it step by step when they are mentioned)

3. Install `WeChat-3.9.5.81.exe` on your computer, **if your version is higher than 3.9.5.81, you can downgrade instantly, or install seperately in other directory**. Afterwards, please **start it as an administrator** and log in. **If you want to dual-open WeChat, you need to install two different versions and modify `./dual-start.bat` according to the comments **, the subsequent steps are slightly different, please continue to read [here](. /doc/Dual_Start.md).

   

4. Monitoring WeChat message by running a server. It has been modified to 1 solution after version V1.20:

   ```bash
   >  cd .\wxinject\bin\
   >  .\injector.exe -n WeChat.exe -i .\wxinject.dll
   ```
   
   
   
5. The last step is fill json files listed in `.config/` . 

   - In `api_config.json`, you need to fill in your own parameter settings for API calls. If you don’t know the specific parameters, you only need to fill in the "api_key" and optional "proxy" items.

   - In `server_config.json`, you can customize the listening address and port. If you don’t know it exactly, no modification needed by default.

   - In `config.json` ,  you need to configure your custom options based on your preferences.

   - In `sys_character.json`, you can customize the character the bot needs to play, and use the command to activate when chatting.

     

6. Run `main.py` by using command:

   ```
   python main.py
   ```

   **Everything is ready, feel free to go online with your ChatGPT-weBot !** 
   
   No limitation, but since switching to OpenAI API, there are usage counts and payment requirements.





## Q&A

1. How to get all response? You can say "continue" in your language.

2. Have problems? Feel free to create an issue.

3. How to trace problems in multithreaded program? Print or using debug with information of thread-stack.

4. Have any preview images related to functionality? Yes, go to -> [Preview](./doc/Preview.md)

5. Wanna buy me coffee? Thank you, qrcode is as follows.

   ![image-20230321150123666](assets/image-20230321150123666.png)

   



## Who has starred

[![Stargazers repo roster for @SnapdragonLee/ChatGPT-weBot](https://reporoster.com/stars/dark/SnapdragonLee/ChatGPT-weBot)](https://github.com/SnapdragonLee/ChatGPT-weBot/stargazers)



## Stargazers over time

[![Stargazers over time](https://starchart.cc/SnapdragonLee/ChatGPT-weBot.svg)](https://starchart.cc/SnapdragonLee/ChatGPT-weBot) 




###### Reference

- [AutumnWhj/ChatGPT-wechat-bot: ChatGPT for wechat](https://github.com/AutumnWhj/ChatGPT-wechat-bot)
- [cixingguangming55555/wechat-bot: 带二次开发接口的PC微信聊天机器人](https://github.com/cixingguangming55555/wechat-bot)
