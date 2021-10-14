Requesting a Cloud Shell.Succeeded.
Connecting terminal...

Welcome to Azure Cloud Shell

Type "az" to use Azure CLI
Type "help" to learn about Cloud Shell

dmitriy@Azure:~$ az aks create --resource-group new-virtual-machine_group --name new-cluster-group --node-count 1 --generate-ssh-keys
SSH key files '/home/dmitriy/.ssh/id_rsa' and '/home/dmitriy/.ssh/id_rsa.pub' have been generated under ~/.ssh to allow SSH access to the VM. If using machines without permanent storage like Azure Cloud Shell without an attached file share, back up your keys to a safe location
Resource provider 'Microsoft.ContainerService' used by this operation is not registered. We are registering for you.
Registration succeeded.
 \ Running ..
{
  "aadProfile": null,
  "addonProfiles": null,
  "agentPoolProfiles": [
    {
      "availabilityZones": null,
      "count": 1,
      "enableAutoScaling": null,
      "enableEncryptionAtHost": false,
      "enableFips": false,
      "enableNodePublicIp": false,
      "enableUltraSsd": false,
      "gpuInstanceProfile": null,
      "kubeletConfig": null,
      "kubeletDiskType": "OS",
      "linuxOsConfig": null,
      "maxCount": null,
      "maxPods": 110,
      "minCount": null,
      "mode": "System",
      "name": "nodepool1",
      "nodeImageVersion": "AKSUbuntu-1804gen2containerd-2021.09.29",
      "nodeLabels": null,
      "nodePublicIpPrefixId": null,
      "nodeTaints": null,
      "orchestratorVersion": "1.20.9",
      "osDiskSizeGb": 128,
      "osDiskType": "Managed",
      "osSku": "Ubuntu",
      "osType": "Linux",
      "podSubnetId": null,
      "powerState": {
        "code": "Running"
      },
      "provisioningState": "Succeeded",
      "proximityPlacementGroupId": null,
      "scaleDownMode": null,
      "scaleSetEvictionPolicy": null,
      "scaleSetPriority": null,
      "spotMaxPrice": null,
      "tags": null,
      "type": "VirtualMachineScaleSets",
      "upgradeSettings": null,
      "vmSize": "Standard_DS2_v2",
      "vnetSubnetId": null
    }
  ],
  "apiServerAccessProfile": null,
  "autoScalerProfile": null,
  "autoUpgradeProfile": null,
  "azurePortalFqdn": "new-cluste-new-virtual-mach-829be2-cd8d5d66.portal.hcp.eastus.azmk8s.io",
  "disableLocalAccounts": null,
  "diskEncryptionSetId": null,
  "dnsPrefix": "new-cluste-new-virtual-mach-829be2",
  "enablePodSecurityPolicy": null,
  "enableRbac": true,
  "extendedLocation": null,
  "fqdn": "new-cluste-new-virtual-mach-829be2-cd8d5d66.hcp.eastus.azmk8s.io",
  "fqdnSubdomain": null,
  "httpProxyConfig": null,
  "id": "/subscriptions/829be2fa-8e06-4d38-b363-2baa3aa22500/resourcegroups/new-virtual-machine_group/providers/Microsoft.ContainerService/managedClusters/new-cluster-group",
  "identity": {
    "principalId": "0e36f117-e87f-4c5c-8a6d-11b10515d8c7",
    "tenantId": "8cc5d2c9-3b51-47e8-befa-ea08c1d1aae3",
    "type": "SystemAssigned",
    "userAssignedIdentities": null
  },
  "identityProfile": {
    "kubeletidentity": {
      "clientId": "df987901-3723-400f-9eab-f11ad056d5d8",
      "objectId": "e4adc428-8270-4870-8757-c5dc82ff34f3",
      "resourceId": "/subscriptions/829be2fa-8e06-4d38-b363-2baa3aa22500/resourcegroups/MC_new-virtual-machine_group_new-cluster-group_eastus/providers/Microsoft.ManagedIdentity/userAssignedIdentities/new-cluster-group-agentpool"
    }
  },
  "kubernetesVersion": "1.20.9",
  "linuxProfile": {
    "adminUsername": "azureuser",
    "ssh": {
      "publicKeys": [
        {
          "keyData": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDFahSwKcEhTOiu5sjEBp2Sz4C2MsREZvXdRMIsrnVBdBLMc1qIXUM2z0S+bIyu9tr0bBmSeiiUQye27TFZhEApKbQOrab8+cOr1mmkSAvaJ167hCAhBKbmaMluzMQlcy3gcvtkrmpjWci/hEtywvwkqI5b1NTBpLmGOpnPqCSdTCoI8tKoy4F9sUmNJ1Wj87Yc9oPi9ak1uy2wimeZT4xigXIj/yQKRppQdNKGwKUv76+geR36h1uC3bmU2IX6fFr7HkzH1fH+TndZiswmSpmlISoGvM+eBKOM4NeNdu0ijFBiCyir4SiVYs7u9CPTsr4DgdVjyrwKZUgNz0qrgyer"
        }
      ]
    }
  },
  "location": "eastus",
  "maxAgentPools": 100,
  "name": "new-cluster-group",
  "networkProfile": {
    "dnsServiceIp": "10.0.0.10",
    "dockerBridgeCidr": "172.17.0.1/16",
    "loadBalancerProfile": {
      "allocatedOutboundPorts": null,
      "effectiveOutboundIPs": [
        {
          "id": "/subscriptions/829be2fa-8e06-4d38-b363-2baa3aa22500/resourceGroups/MC_new-virtual-machine_group_new-cluster-group_eastus/providers/Microsoft.Network/publicIPAddresses/2d4f83a5-bdd5-41ae-90c2-11a310d15645",
          "resourceGroup": "MC_new-virtual-machine_group_new-cluster-group_eastus"
        }
      ],
      "idleTimeoutInMinutes": null,
      "managedOutboundIPs": {
        "count": 1
      },
      "outboundIPs": null,
      "outboundIpPrefixes": null
    },
    "loadBalancerSku": "Standard",
    "natGatewayProfile": null,
    "networkMode": null,
    "networkPlugin": "kubenet",
    "networkPolicy": null,
    "outboundType": "loadBalancer",
    "podCidr": "10.244.0.0/16",
    "serviceCidr": "10.0.0.0/16"
  },
  "nodeResourceGroup": "MC_new-virtual-machine_group_new-cluster-group_eastus",
  "podIdentityProfile": null,
  "powerState": {
    "code": "Running"
  },
  "privateFqdn": null,
  "privateLinkResources": null,
  "provisioningState": "Succeeded",
  "resourceGroup": "new-virtual-machine_group",
  "securityProfile": null,
  "servicePrincipalProfile": {
    "clientId": "msi",
    "secret": null
  },
  "sku": {
    "name": "Basic",
    "tier": "Free"
  },
  "tags": null,
  "type": "Microsoft.ContainerService/ManagedClusters",
  "windowsProfile": null
}
