09-26-2025
Note Type: #Permanent 
Note Maturity: 
Topic Tags: #Sentinel

# Notes
When using Azure Sentinel, we have the ability to create and manage multiple workspaces within the Sentinel environment. 

The main building block of Sentinel's platform are called [[Sentinel Workspace]]. 

When setting up Sentinel you need to plan how you desire to manage your Sentinel Workspace. There are three general configurations that you can setup for Sentinel Workspaces. 
- Single Tenant, Single Workspace
- Single Tenant, Multi Workspace.
- Multi-Tenant Workspaces

The Single Tenant, Single Workspace is the simplest configuration. This is truly just a single Azure instance that is configured with a Single Workspace. This is the easiest to setup and manage. In this configuration, you have a single pane of glass where you can administer your Sentinel Workspaces. The biggest drawbacks for using this may have some scalability constraints. This configuration is best suited for small-medium business where they have highly localized assets. There are constraints and limitations when it comes to moving data across regions. There is also a concern for data sovereignty when using 
Workspaces can be linked together by using [[Workspace Manager]].
# Reference


# Links
[[SC-200 Fleeting Notes]]