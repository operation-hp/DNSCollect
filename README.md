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


https://github.com/operation-hp/DNSCollect/assets/132428527/005239ee-6590-40b6-bb45-2c8f8ad5e1c5




## Case Demo 
### Login Failed Monitoring (EventID 4625)
When someone tries to log in to your device but fails, the task schedule will start the event and send a record to Our DNS Server.


https://github.com/operation-hp/DNSCollect/assets/132428527/a67a1e36-7cb4-46dc-94c8-4c8d77f91c57


### Change of Account setting Monitoring (EventID 4732)
Changing the setting of any account will trigger our events and send a record to Our DNS Server. If you do not have any memory for those changes, please pay attention to your device to see if it has been accessed unauthorizedly.



https://github.com/operation-hp/DNSCollect/assets/132428527/3638044d-6486-4b7a-9200-b2f9985a70a0



DNSCollect is sponsored by AP Lens (Whitelist DNS Firewall with Web Proxy)
