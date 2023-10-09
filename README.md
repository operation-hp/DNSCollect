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



DNSCollect 得到 AP Lens 的贊助（白名單DNS防火墻與Web代理）。


