# Net Zero Cloud - Permission Sets for Tab Visibility

Contains two permission sets, one for Starter and one for Growth, that turn on tab visibility for ALL objects. You do not need to use both perm sets, just choose whichever is right for your edition. 

To deploy, you can either

1) Load the perm set using SFDX into your org and assign them to the right users.

OR 

2) In a text editor, copy and paste the tab visibility xml to the permission set(s) you are already using and then deploy to sfdx. 

The xml looks like this:

    <tabSettings>
    	<tab>standard-RefrigerantEmssnFctr</tab>
    	<visibility>Visible</visibility>
    </tabSettings>

Note that the perm set you put the XML in has to be attached to the Net Zero Cloud License.

### some useful sfdx commands

to retrieve all permission sets:

	$ sfdx force:source:retrieve -m PermissionSet

to deploy a single file: 

	$ sfdx force:source:deploy -p force-app/main/default/permissionsets/Net_Zero_Growth_Tab_Permissions.permissionset-meta.xml

## Read More

- [Net Zero Cloud](https://www.salesforce.com/products/net-zero-cloud/overview)
- [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_intro.htm)
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference.htm)
