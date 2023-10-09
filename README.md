# [English Version](#why-dnscollect)

# [中文版](#為什麼選擇-dnscollect)



# DNSCollect is an agent-less tool crafted explicitly for remote Windows 10 event log collection.

## Why DNSCollect? 

<img width="763" alt="DNSCollect-intro" src="https://github.com/operation-hp/DNSCollect/assets/51909803/ed3aee93-b65b-43f1-85de-a6ccd33e00b1">

Windows Event Log triggers a ping command with the event as the subdomain when a high-risk event happens. The domain does not exist, but the DNS query is stored in the DNS log and can be used to generate alerts. 

- **Supply Chain Safety**: Supply chain attacks are increasingly frequent; DNSCollect offers an agent-less approach, reducing potential vulnerabilities.

- **Remote Collections**: DNSCollect capitalizes on DNS queries, enabling seamless remote event log collections without needing installations or intrusive permissions.

It is still in beta and will benefit from real-world testing. If you're in cybersecurity or just curious, we'd appreciate it if you could take DNSCollect for a spin. Your feedback can be invaluable in refining and enhancing this tool for the community.

## Installation of DNSCollect in Task Scheduler.
- Open the Task Scheduler in Windows
- Select "Import Task"
- Choose the event file we provided for you
- In "Change User or Group," and type Administrators to run this task
- Go to "Settings" and choose the setting from "Do not start a new instance" to "Stop the existing instance." Otherwise, the task will stuck in the previous instance
- Go to "Actions" and choose the cmd.bat file
- Finished


https://github.com/operation-hp/DNSCollect/assets/132428527/ab2e04ea-41fb-462a-8e47-2e3df0d85f2b



## Case Demo 
### Login Failed Monitoring (EventID 4625)
When someone tries to log in to your device but fails, the task schedule will start the event and send a record to Our DNS Server.


https://github.com/operation-hp/DNSCollect/assets/132428527/dcbb0b9e-aa48-4ceb-8ffc-ee918aa9b325


### Change of Account setting Monitoring (EventID 4732)
Changing the setting of any account will trigger our events and send a record to Our DNS Server. If you do not have any memory for those changes, please pay attention to your device to see if it has been accessed unauthorizedly.


https://github.com/operation-hp/DNSCollect/assets/132428527/0b052aa3-db9d-49b4-b3f2-e55e8007f1f3

## FAQ
## How can I open Task Scheduler in Windows?
- You can use the "Search" function and type "Task Scheduler"
- You can also press "Windows + R" to open the Run window and type this command "taskschd.msc"

## What is an EventID, and why is it important in DNSCollect?
- An EventID is a unique identifier assigned to specific events in the Windows Event Log. It's important in DNSCollect because certain EventIDs trigger actions and alerts within the tool.

## Can I customize DNSCollect to respond to different EventIDs?
- DNSCollect allows some degree of customization to specify actions for specific EventIDs. You can configure it to react differently based on your monitoring needs.

## How can I troubleshoot issues related to EventID monitoring with DNSCollect?
- If you encounter problems with DNSCollect's EventID monitoring, consult the tool's documentation or community support resources for troubleshooting guidance.


DNSCollect is sponsored by AP Lens (Whitelist DNS Firewall with Web Proxy)



# DNSCollect 是一個特別為遠程 Windows 10 事件日誌收集而設計的無需代理工具。

## 為什麼選擇 DNSCollect？ 

<img width="763" alt="DNSCollect-intro" src="https://github.com/operation-hp/DNSCollect/assets/51909803/ed3aee93-b65b-43f1-85de-a6ccd33e00b1">

當發生高風險事件時，Windows事件日誌會以事件作為子域名觸發ping命令。該域名不存在，但DNS查詢會存儲在DNS日誌中，可用於生成警報。

- **供應鏈安全**: 供應鏈攻擊日益頻繁；DNSCollect 提供無需代理的方法，降低了潛在的漏洞風險。


- **遠程收集**: DNSCollect 利用 DNS 查詢，實現無需安裝或入侵性權限的無縫遠程事件日誌收集。

它仍然處於測試階段，將從實際測試中受益。如果您是網絡安全專業人員，或者只是好奇的話，我們將不勝感激，如果您能試用 DNSCollect。您的反饋對於完善和增強這個工具對社區來說非常寶貴。

## 在任務計劃程序中安裝 DNSCollect。
- 打開 Windows 的任務計劃程序
- 選擇 "匯入任務"
- 選擇我們為您提供的事件文件
- 在 "更改用戶或組" 中，輸入 "Administrators" 以運行此任務
- 轉到 "設置"，從 "不啟動新實例" 選擇到 "停止現有實例"。否則，任務將卡在之前的實例中
- 轉到 "操作"，選擇 cmd.bat 文件
- 完成


https://github.com/operation-hp/DNSCollect/assets/132428527/ab2e04ea-41fb-462a-8e47-2e3df0d85f2b



## 案例演示
### 登錄失敗監控（事件ID 4625）
當有人嘗試登錄您的設備但失敗時，任務計劃將啟動事件並將記錄發送到我們的DNS服務器。


https://github.com/operation-hp/DNSCollect/assets/132428527/dcbb0b9e-aa48-4ceb-8ffc-ee918aa9b325


### 帳戶設置更改監控（事件ID 4732）
更改任何帳戶的設置將觸發我們的事件並將記錄發送到我們的DNS服務器。如果您對這些更改沒有記憶，請注意您的設備是否已被未經授權訪問。


https://github.com/operation-hp/DNSCollect/assets/132428527/0b052aa3-db9d-49b4-b3f2-e55e8007f1f3

## 常見問題
## 什麼是事件ID，以及在DNSCollect中為什麼如此重要？
- 事件ID是分配給Windows事件日誌中特定事件的唯一標識符。在DNSCollect中，某些事件ID會觸發工具內的操作和警報，因此具有重要性。

## 我可以自定義DNSCollect以對不同的事件ID做出回應嗎？
- DNSCollect允許在某種程度上自定義，以指定對特定事件ID做出回應的操作。您可以根據您的監控需求配置它，使其根據需要以不同方式作出反應。

## 如何解決與DNSCollect事件ID監控相關的問題？
- 如果您在使用DNSCollect的事件ID監控過程中遇到問題，請參考工具的文檔或社區支援資源，以獲得故障排除指南。

## 如何在Windows中打開Task Scheduler？
- 您可以使用"搜尋"功能，然後輸入"Task Scheduler"。
- 您也可以按下"Windows + R"來打開執行視窗，然後輸入這個命令"taskschd.msc"。

DNSCollect 得到 AP Lens 的贊助（白名單DNS防火墻與Web代理）。


