# Distributed under the MIT License
Downloading the solution components constitutes acceptance of the MIT license within this repository.

# Copilot Studio ServiceNow Agent
This solution comprises of a Copilot Studio based self-service agent that connects to a Service Now instance under user context using basic authentication. It responds to questions about Requests, Catalog tasks, RITMs. It responds to natural language instructions with follow up question capabilities. It executes the queries against SNOW and renders output in a easy to consume manner. 


# Copilot Studio Agent – Solution Import Instructions

This guide explains how to import the **Copilot Studio Agent** solution into your Power Platform environment and configure the ServiceNow connection.

---

## Prerequisites

- Access to a **Power Platform environment** with proper permissions.
- The **solution `.zip` file** containing the Copilot Studio Agent.
- Credentials and access for **ServiceNow** instance to set up the connection.

---

## Step 1: Import the Solution

1. Log in to your Power Platform environment:  
   [https://make.powerapps.com](https://make.powerapps.com)

2. In the left-hand navigation, select **Solutions**.

3. Click **Import** at the top of the page.

4. Browse and select the **Copilot Studio Agent solution `.zip` file**.

5. Click **Next**, then **Import**.

> ⚠️ The import may take a few minutes. Wait for the process to complete before proceeding.

---

## Step 2: Verify Solution Components

- Open the solution after import.
- Confirm the following components are present:
  - **Copilot Studio Agent** (Power Platform Agent)
  - **Flows** (if included in the package)
  - **Environment variables** (if any)

---

## Step 3: Configure the ServiceNow Connection

The agent requires a single **ServiceNow connection**:

1. In the solution, locate the **ServiceNow connection reference**.  
   Typically, this appears under **Connections** or **Connection References**.

2. Click the connection reference and choose **Edit Connection**.

3. Enter your **ServiceNow instance URL** and credentials:
   - Username / Password (or OAuth if configured)
   - Instance URL (e.g., `https://your-instance.service-now.com`)

4. Save the connection.

> ⚠️ If the connection fails, verify that your ServiceNow account has **API access** and the correct permissions for the tables/actions used by the agent.

---

## Step 4: Publish All Customizations

- After configuring the ServiceNow connection, click **Publish All Customizations** in the solution to apply changes.

---

## Step 5: Verify Functionality

1. Open the **Copilot Studio Agent** in your environment.
2. Test basic functionality to ensure it connects to ServiceNow and responds as expected.
3. Verify any flows or actions triggered by the agent work correctly.

---

## Troubleshooting

- **Connection errors**: Re-enter ServiceNow credentials and ensure the account has proper API access.  
- **Agent not responding**: Check flows and triggers in the solution, and republish if necessary.  
- **Environment variable issues**: Ensure all required variables have valid values.

---

## Additional Resources

- [Power Platform Solutions Documentation](https://learn.microsoft.com/power-platform/solutions/overview)  
- [Manage Connections in Power Platform](https://learn.microsoft.com/power-platform/admin/connections)  
- [ServiceNow REST API Documentation](https://developer.servicenow.com/dev.do#!/reference/api)
