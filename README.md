# Salesforce DX Project: Next Steps

Now that you’ve created a Salesforce DX project, what’s next? Here are some documentation resources to get you started.

## How Do You Plan to Deploy Your Changes?

Do you want to deploy a set of changes, or create a self-contained application? Choose a [development model](https://developer.salesforce.com/tools/vscode/en/user-guide/development-models).

## Configure Your Salesforce DX Project

The `sfdx-project.json` file contains useful configuration information for your project. See [Salesforce DX Project Configuration](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_ws_config.htm) in the _Salesforce DX Developer Guide_ for details about this file.

## Read All About It

- [Salesforce Extensions Documentation](https://developer.salesforce.com/tools/vscode/)
- [Salesforce CLI Setup Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_intro.htm)
- [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_intro.htm)
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference.htm)

## -------------------INSTRUCTION THAT SHOULD FOLLOW BEFORE PUSHING SOURCE TO ANY ORG-------------------
Follow following instruction to avoid respective error mentioned below:
    *Invalid FLow Version
        ->Go under Flow Definition -> change activeVersionNumber to 1
   
    *filterlanguage: invalid value specified:
        ->Go to Org -->Setup--> Translation Workbench -->Translation language settings-->Enable
   
    *invalid cross reference id
        ->force-app\main\default-->Application-->SelectApp-->remove all
          <profileActionOverrides> tags except those which contains:-
            <profile>Admin</profile> or <profile>Standard</profile>
    	Note: It should contains only those profiles which is already there in the targeted org.
