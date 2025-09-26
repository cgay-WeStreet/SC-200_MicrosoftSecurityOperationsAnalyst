09-26-2025
Note Type:
Note Maturity:
Topic Tags:

# Notes
- If you are setting up Defender for Cloud (Which I think is Sentinel) in AWS, there appears to be different plans available for securing AWS Workloads. These need to be properly evaluated before implementing them. 
- Overall, for connecting Defender for Cloud to a third-party cloud platform, the configuration is; get administrative privileges for the third-party cloud platform, pick the Defender for Cloud plan that we want to use, configure access to the platform, done.
- Alerts in Defender for Cloud do appear to be highly comparable to Alerts in O365's Investigation and Response tab.

### [[Planning Sentinel]]
- There are three implementation options  for Sentinel
	- Single Tenant, Single Workplace
		- Con
			- There is a Cross-region bandwidth cost concern
			- Data Governance concerns.
	- Single Tenant, Regional Workspaces
		- The name describes what it is. It's A single Tenant that uses multiple workspaces for its workloads.
		- Cons
			- No central pane of glass, multiple workspaces will force 
	- Multi Tenant Workspaces
		- Must use Azure Lighthouse to use multi-tenant as an orchestrator

### Creating a Sentinel workspace
- **Note**: I do believe that Sentinel is divorced from Azure. This may be wrong.
- [[How to create a Sentinel Workspace]]
	- Navigate to Azure.
	- Search for Sentinel in the search bar, there may be a manual path but I couldn't find it.
	- Click "Create"
	- Click Create a new workspace.
	- Fill in the info.
	- **This does cost money!**

### Sentinel Configuration
- Settings is where you can pick your pricing options.
- You have the ability to increase your Data Retention through the Usage and Estimation costs.
#### Tables in Sentinel
- In Sentinel, you are able to view and edit the tables that Sentinel queries by accessing the tables setting.
- You can modify the retention period for tables very granularly.

### Sentinel Roles
#### Sentinel Specific Roles
- Microsoft Sentinel Reader - View only access to data, incidents, and workbooks
- Microsoft Sentinel Responder - Has all permissions as Microsoft Sentinel Reader, plus Assigning incidents, Dismissing incidents, general management of incidents.
- Microsoft Sentinel Contributor - Has all permissions as Sentinel Reader and Responder, plus the ability to Install and update Solutions from the Content Hub, Create and Edit workbooks and Analytic Rules and etc?
- Microsoft Playbook Operator - Allows them to List view and Manually run Playbooks. 
- Microsoft Automation Contributor - Adds Playbooks to automation rules. 
	- **This is not a user role**

##### Azure Roles linked to Sentinel
- Logic Apps Contributor -

#### Role Recommendations
- **Security Analysts** are recommended to have the Sentinel Responder and Playbook Operator roles.
	- Does the lower level work for Security Incidents.
- **Security Engineer** would use the Microsoft Sentinel Contributor and Logic Apps Contributor role.
	- This role creates the tools that the Analysts use to perform their tasks.
- **Service Principal** - Use Microsoft Sentinel Contributor.
	- This seems to be like a service account role in Sentinel.
### Multiple Sentinel Workspaces
- You will need the Contributor role in all workspaces that you are linking.
- Azure Lighthouse to connect the multi-tenants if you have multi-tenant.

#### Architecture
- Three general architectures: Simple/Direct Link, Co-Management, and N-tier Architecture
	- Simple/Direct Link
		- This is like a hub and spoke configuration. A single source workspace controls all other workspaces. 
	- Co-Management
		- Common in MSSP setups where multiple Administrators will need to manage a Sentinel Workspace.
		- You will have two "Hub" Sentinel workspaces configured to control a shared workspace. So in essence you have a single spoke connected to two hubs.
	- N-Tier 
		- This is nested hub and spoke. You have a "Child" hub and spoke setup with the Hub being managed by a parent Hub. That parent hub will manage other subordinate hubs as a central control point. 
# Reference


# Links
