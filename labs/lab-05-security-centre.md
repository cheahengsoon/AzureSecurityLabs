# Lab 5 – Azure Security Center for security recommendations

## Understand your application security posture in Azure

First thing is to upgrade your subscription to the Standard Tier to get all features of Azure Security Center.

### 5.1 - Enable your Azure subscription

1. Sign into the Azure portal.
2. On the Microsoft Azure menu, select **Security Center**. The **Security Center - Overview** opens.

![oms](/images/OMS.png)

**Security Center – Overview** provides a unified view into the security posture of your hybrid cloud workloads, enabling you to discover and assess the security of your workloads and to identify and mitigate risk. Security Center automatically enables any of your Azure subscriptions not previously onboarded by you or another subscription user to the Free tier.

You can view and filter the list of subscriptions by clicking the Subscriptions menu item. Security Center will now begin assessing the security of these subscriptions to identify security vulnerabilities. To customize the types of assessments, you can modify the security policy. A security policy defines the desired configuration of your workloads and helps ensure compliance with company or regulatory security requirements.

Within minutes of launching Security Center the first time, you may see:

- **Recommendations** for ways to improve the security of your Azure subscriptions. Clicking the Recommendations tile will launch a prioritized list.
- An inventory of **Compute & apps, Networking, Data security, and Identity & Access** resources that are now being assessed by Security Center along with the security posture of each.

To take full advantage of Security Center, you need to complete the steps below to upgrade to the Standard tier and install the Microsoft Monitoring Agent.

### 5.2 - Upgrade to the Standard tier

For the purpose of the Security Center quickstarts and tutorials you must upgrade to the Standard tier. Your first 60 days are free, and you can return to the Free tier any time.

1. Under the Security Center main menu, select **Onboarding to advanced security**
2. Under Onboarding to advanced security, Security Center lists subscriptions and workspaces eligible for onboarding. Select a subscription from the list.

    ![oms advanced](/images/oms-advanced.png)

3. Security policy provides information on the resource groups contained in the subscription. Pricing also opens.
4. Under Pricing, select Standard to upgrade from Free to Standard and click Save.

![oms pricing](/images/oms-pricing.png)

Now that you’ve upgraded to the Standard tier, you have access to additional Security Center features, including **adaptive application controls, just in time VM access, security alerts, threat intelligence, automation playbooks**, and more. Note that security alerts will only appear when Security Center detects malicious activity.

![oms global](/images/oms-global.png)

### 5.3 - Automate data collection

Security Center collects data from your Azure VMs and non-Azure computers to monitor for security vulnerabilities and threats. Data is collected using the Microsoft Monitoring Agent, which reads various security-related configurations and event logs from the machine and copies the data to your workspace for analysis. By default, Security Center will create a new workspace for you.
When automatic provisioning is enabled, Security Center installs the Microsoft Monitoring Agent on all supported Azure VMs and any new ones that are created. Automatic provisioning is strongly recommended.
To enable automatic provisioning of the Microsoft Monitoring Agent:

1. Under the Security Center main menu, select **Security Policy**.
2. Select the subscription.
3. Under **Security policy**, select **Data Collection**.
4. Under **Data Collection**, select **On** to enable automatic provisioning.
5. Click **Save**.

![oms datacollection](/images/oms-datacollection.png)

With this new insight into your Azure VMs, Security Center can provide additional recommendations related to system update status, Operating System security configurations, endpoint protection, as well as generate additional security alerts.

![oms recomm](/images/oms-recomm.png)

<< [Back to home page](/README.md)

<< [Previous Lab](lab-04-app-gateway.md) . . . . . [Next Lab](lab-06-storage-security.md) >>