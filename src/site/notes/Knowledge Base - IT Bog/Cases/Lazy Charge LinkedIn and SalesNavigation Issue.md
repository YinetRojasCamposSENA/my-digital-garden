---
{"dg-publish":true,"permalink":"/knowledge-base-it-bog/cases/lazy-charge-linked-in-and-sales-navigation-issue/","tags":["gardenEntry"]}
---

On May, Tuesday 6th, in the morning, various persons report a lazy charge in LinkedIn and SalesNavigation. 

## **1. Issue Description**

Multiple users report persistent problems accessing LinkedIn, including:

- Slow loading times.
    
- Connection errors (e.g., "Something went wrong," HTTP 500).
    
- Inability to load profiles/messages.
    

**Verified Non-Issues**:

- LinkedIn’s status page shows no global outages.
    
- Problems persist **even with**:
    
    - VPN (OpenVPN) disabled.
        
    - Wired Ethernet connection.
        
    - Different browsers (Chrome, Firefox, Edge).
## **2. Root Cause Analysis**

### **Possible Causes**

|**Category**|**Potential Cause**|**Validation Steps**|
|---|---|---|
|**Network**|Corporate firewall/proxy blocking LinkedIn domains.|Test access on a non-corporate network (e.g., mobile hotspot).|
|**DNS**|Misconfigured DNS resolving LinkedIn domains incorrectly.|`nslookup www.linkedin.com` (compare results on VPN vs. no VPN).|
|**Browser**|Extensions (ad-blockers) or cached data interfering.|Test in Incognito mode + disabled extensions.|
|**Google Workspace**|Admin policies restricting social media access (e.g., DLP rules).|Check `Admin Console > Security > Access controls`.|
|**OpenVPN**|VPN routing conflicts (even when disabled, residual settings may apply).|Test on a device that **never** connected to VPN.|