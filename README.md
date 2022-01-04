# Citrix-Virtual-Apps-and-Desktops-V3
	Creates an inventory of a Citrix Virtual Apps and Desktops (CVAD) 2006 or later Site 
	using Microsoft PowerShell, Word, plain text, or HTML.
	
	This script requires at least PowerShell version 5.

	Default output is now HTML.
	
	You do NOT have to run this script on a Controller. This script was developed and run 
	from a Windows 10 VM.
	
	You can run this script remotely using the –AdminAddress (AA) parameter.
	
	This script supports versions of CVAD starting with 2006.
	
	If you are running XA/XD 7.0 through 7.7, please use: 
	https://carlwebster.com/downloads/download-info/xenappxendesktop-7-x-documentation-script/

	If you are running XA/XD 7.8 through CVAD 2006, please use:
	https://carlwebster.com/downloads/download-info/xenappxendesktop-7-8/

	If you are running Citrix Cloud, please use:
	https://carlwebster.com/downloads/download-info/citrix-cloud-citrix-virtual-apps-and-desktops-service/
	
	NOTE: The account used to run this script must have at least Read access to the SQL 
	Server(s) that hold(s) the Citrix Site, Monitoring, and Logging databases.
	
	By default, only gives summary information for:
		Administrators
		App-V Publishing
		Application Groups
		Applications
		Controllers
		Delivery Groups
		Hosting
		Logging
		Machine Catalogs
		Policies
		StoreFront
		Zones

	The Summary information is what is shown in the top half of Citrix Studio for:
		Machine Catalogs
		Delivery Groups
		Applications
		Policies
		Logging
		Controllers
		Administrators
		Hosting
		StoreFront

	Using the MachineCatalogs parameter can cause the report to take a very long time to 
	complete and can generate an extremely long report.
	
	Using the DeliveryGroups parameter can cause the report to take a very long time to 
	complete and can generate an extremely long report.

	Using both the MachineCatalogs and DeliveryGroups parameters can cause the report to 
	take an extremely long time to complete and generate an exceptionally long report.
	
	Using BrokerRegistryKeys requires the script runs elevated.

	Creates an output file named after the CVAD Site.
	
	Word and PDF Document includes a Cover Page, Table of Contents and Footer.
	Includes support for the following language versions of Microsoft Word:
		Catalan
		Chinese
		Danish
		Dutch
		English
		Finnish
		French
		German
		Norwegian
		Portuguese
		Spanish
		Swedish
		
NOTE: This script requires PowerShell V5 or later.
Support for non-English Versions of Microsoft Word
The script supports the following languages:
•	Catalan
•	Chinese
•	Danish
•	Dutch
•	English
•	Finnish
•	French
•	German
•	Norwegian
•	Portuguese
•	Spanish
•	Swedish

Prerequisites
Let us ensure we have the requirements before using PowerShell to document anything in a Citrix Virtual Apps and Desktops (CVAD) Site.
1.	If the script runs remotely, there are two choices: install Citrix Studio or manually install the PowerShell snapins.
a.	Install Studio from the full CVAD 2006 or later installation media. Installing Citrix Studio installs all the necessary PowerShell snapins.
b.	Install the PowerShell snapins individually. Depending on the bitness of the computer, from the full CVAD 2006 or later installation media, install the following files from either x64 or x86 (?? is either 86 or 64):
i.	Citrix Desktop Delivery Controller\ADIdentity_PowerShellSnapIn_x??
ii.	Citrix Desktop Delivery Controller\Analytics_PowerShell_SnapIn_x??
iii.	Citrix Desktop Delivery Controller\AppLibrary_PowerShell_SnapIn_x??
iv.	Citrix Desktop Delivery Controller\Azure_Provisioning_SnapIn_x??
v.	Citrix Desktop Delivery Controller\Broker_PowerShell_SnapIn_x??
vi.	Citrix Desktop Delivery Controller\Configuration_PowerShell_SnapIn_x??
vii.	Citrix Desktop Delivery Controller\ConfigurationLogging_PowerShell_SnapIn_x??
viii.	Citrix Desktop Delivery Controller\DelegatedAdmin_PowerShellSnapIn_x??
ix.	Citrix Desktop Delivery Controller\EnvTest_PowerShell_SnapIn_x??
x.	Citrix Desktop Delivery Controller\Host_PowerShell_SnapIn_x??
xi.	Citrix Desktop Delivery Controller\MachineCreation_PowerShellSnapIn_x??
xii.	Citrix Desktop Delivery Controller\Monitor_PowerShellSnapIn_x??
xiii.	Citrix Desktop Delivery Controller\Orchestration_PowerShellSnapIn_x??
xiv.	Citrix Desktop Delivery Controller\Storefront_PowerShellSnapIn_x??
xv.	Citrix Desktop Delivery Controller\Trust_PowerShellSnapIn_x??
xvi.	Citrix Desktop Delivery Controller\UserProfileManager_PowerShellSnapIn_x??
xvii.	Citrix Desktop Delivery Controller\XDPoshSnapin_x??
xviii.	Citrix Policy\CitrixGroupPolicyManagement_x??
xix.	DesktopStudio\PVS PowerShell SDK x??
xx.	DesktopStudio\PzAppV_Studio_PowershellSnapin_x??
xxi.	Licensing\LicensingAdmin_PowerShellSnapIn_x??

Script Usage
How to use this script?
1.	Save the script as CVAD_Inventory_V3.ps1 in your PowerShell scripts folder.
2.	From the PowerShell prompt, change to your PowerShell scripts folder.
3.	From the PowerShell prompt, type in:
a.	.\CVAD_Inventory_V3.ps1 and press Enter.
4.	By default, an HTML document is created named after the CVAD 2006 or later Site.
5.	If you use the –MSWord option, a Microsoft Word file is created named after the CVAD 2006 or later Site.
6.	If you use the –PDF option, a PDF file is created named after the CVAD 2006 or later Site.
7.	If you use the –Text option, a Text file is created named after the CVAD 2006 or later Site.
To run the script on a remote Controller:
.\CVAD_Inventory_V3.ps1 -AdminAddress DDCName and press Enter.
Full help text is available.
Get-Help .\CVAD_Inventory_V3.ps1 –full

The help text explains all the parameters the script accepts.
