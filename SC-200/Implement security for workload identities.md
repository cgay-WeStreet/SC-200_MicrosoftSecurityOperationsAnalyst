Note Type: #Reference
Tags: #SC-200 #MicrosoftDefender 
# Summary

# Notes

## Introduction 

Workload identities, like service accounts and applications are harder to secure due to the normal use of those types of identities. 

These identities often aren't able to MFA, don't have a formal lifecycle, and have their secrets stored somewhere like a password manager for humans to access. 

### Requirements to use workload identity protection

### Note:
*I did not feel this warranted a summary as this is just factual "You have to have these" kinds of things.*

To make use of workload identity risk, including the new Risky workload identities (preview) blade and the Workload identity detections tab in the Risk detections blade, in the Azure portal you must have the following.

- Microsoft Entra ID Premium P2 licensing
    
- Logged in user must be assigned either:
    
    - Security administrator
    - Security operator
    - Security reader
## Types of Risk that are detected

Microsoft Defender can protect Workload Identities by using different signals to indicate potential compromise. 

These are personal definitions, but Defender uses two categories of signals. 
- Threat Intelligence
- Manual

Threat Intelligence are signals from Microsoft Entra's genuine Threat Intelligence service as well as indicators like Suspicious IP addresses and unusual sign ins by user based identities. It also monitors for unusual credentials being added to the workload. 

Manual triggers are just that. Manual. An Admin will go in and say "this is compromised"


# Reference
- [Implement security for workload identities - Training | Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/manage-azure-active-directory-identity-protection/7-implement-security-workload-identities)