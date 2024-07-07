# AZ104Test
This is a test of the AZ104 GitHub Repo

This code is not owned by me. This is from AzureCitadel. I'm using this for Educational purposes. 

I took PIP out of:         {
            "comments": "Create single VM in the on-premises vNet",
            "name": "Deploy-OnPrem-VM",
            "type": "Microsoft.Resources/deployments",
            "apiVersion": "2017-05-10",
            "resourceGroup": "[variables('onprem').resourceGroup]",
            "properties": {
                "mode": "Incremental",
                "templateLink": {
                    "uri": "[variables('vmUri')]",
                    "contentVersion": "1.0.0.0"
                },
                "parameters": {
                    "vNetName": {
                        "value": "[variables('onprem').vnet.name]"
                    },
                    "subnetName": {
                        "value": "[variables('onprem').subnets[1].name]"
                    },
                    "vmName": {
                        "value": "OnPrem-vm"
                    },
                    "script": {
                        "value": "StandardOSUpgrade.sh"
                    },
                    "pip?": {
                        "value": true
                    }
                }
            },
            "dependsOn": [
                "Deploy-OnPrem-vNet"
            ]
        },
