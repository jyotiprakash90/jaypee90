This PowerShell Script Enables/Disables Azure Hybrid Benefit for Virtual Machine/Virtual Machine Scalesets in a given Subbscription/Resource Group or individual Resources.More of AHUB Benefit here : https://azure.microsoft.com/en-us/pricing/hybrid-benefit/

DESCRIPTION

This PowerShell Script Enables/Disables Azure Hybrid Benefit for Virtual Machine/Virtual Machine Scalesets in a given Subbscription/Resource Group or individual Resources.

More on AHUB Benefit here

Savings work only if you already have on-premises Windows Server licenses with Software Assurance.

REQUIRED

1. AzureSubscriptionName - parameter that allows scoping VMs to a particular  Subscription.
3. AzureResourceGroup - parameter to input ResourceGroup name
2. Resource - Choose between VM, VMSS, "VM,VMSS"

OPTIONAL

1. VMSSName - parameter that allows scoping only a particular VMSS (Works with Resource parameter as VMSS)
2. VMName - parameter that allows scoping only a particular VM (Works with Resource parameter as VM)

Example

#Below is the option to Enable AHUB in all VMSS in a particular ResourceGroup

# .\AHUBLicensing.ps1 -AzureSubscriptionName "SubscriptionName" -AzureResourceGroup "ResourceGrpName" -Resource VMSS -LicenseType Windows_Server     

#Below is the option to Disable AHUB in all VM in a particular ResourceGroup

# .\AHUBLicensing.ps1 -AzureSubscriptionName "SubscriptionName" -AzureResourceGroup "ResourceGrpName" -Resource VM -LicenseType None

#Below is the option to Enable AHUB in a single VMSS in a particular ResourceGroup

# .\AHUBLicensing.ps1 -AzureSubscriptionName "SubscriptionName" -AzureResourceGroup "ResourceGrpName" -Resource VMSS -LicenseType Windows_Server -VMSSName "VMSSName"

#Below is the option to Disable AHUB in a single VM in a particular ResourceGroup

# .\AHUBLicensing.ps1 -AzureSubscriptionName "SubscriptionName" -AzureResourceGroup "ResourceGrpName" -Resource VM -LicenseType None -VMName "VMName"



Credits to Pradebban Raja for https://gallery.technet.microsoft.com/scriptcenter/Enable-Disable-Azure-585223ad#content with the original script. 
