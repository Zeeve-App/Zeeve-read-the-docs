---
description: Integrate Hyperledger besu with Zeeve's platform using our API and tools. Our documentation provides technical details on authentication, making requests and handling responses for interacting with Hyperledger besu and the Zeeve platform.
---
# Besu Node Setup
r
This section will guide you about the different features offered by Zeeve for Besu.
<!-- 
 1.  [Dedicated nodes](#dedicated-nodes)
 1.  [Staking nodes](#staking-nodes)

## Dedicated nodes

 1. [Create network](#create-a-network)
 2. [Add a node](#add-node-to-a-network)
 3. [Delete a node](#delete-node-in-a-network)
 4. [Delete network](#delete-a-network) -->

### **Create a network**

This section will provide you with detailed steps for creating a network of **Besu**.

---
***NOTE*** Please make sure to follow the steps mentioned earlier before proceeding.

---


On the **Network Configuration** page you will have different cards with different network configurations for Besu, which looks similar to the image provided below. 

  ![img](./images/CoreumNetworkConfiguration.png)

---
***NOTE:** These cards can be different for your case. Card configurations depend on your purchased subscription.*

---
you can use your cloud account (AWS) for the hosting of your node.

Choose the configuration you want. Click on the card and follow the steps accordingly.

1. **Configure Network:** 
Clicking on the card you will be landed on a page similar to the below image. In this section, we have to provide network-related information for ex- Network Name, Network description, etc.

    ![img](./images/besu/create-besu-step-1.png)

> *   **Network Name**: To uniquely identify your network, this field requires a unique name for it. Unique over here is in terms of the account in which you are creating your network. In case you have created some network earlier, and now you are trying to create with the same name, then the [Zeeve](https://zeeve.io) platform won't allow you to create it.
> *  **Network Description**: Description of the network.
> *  **Namespace**: The kubernetes namespace for the network
> *  **Workspace**: This represents the workspace in which the network will be added after successful creation.

After providing all the details correctly go to the next step by clicking on the **Next Step** button.

2. **Configuration Blockchain:** 
In this section, you have to fill in the details of the blockchain network you want to deploy.

    ![img](./images/besu/create-besu-step-2.png)

> * **Chain ID**: Chain id is require to setup network, it will be added in genesis file of the besu.
> * **Epoch Length**: Epoch length is the duration or period of time during which a specific set of validators or nodes take turns to produce and confirm blocks or transactions on the blockchain.
> * **Block Period Seconds**: Block period seconds is the time interval between the creation of consecutive blocks on a blockchain.
> * **Request Timeout Seconds**: maximum amount of time a node or client is willing to wait for a response from another node or the network when making a blockchain-related request
> * **Consensus Type**: Consensus type in blockchain refers to the agreed-upon method or algorithm used by nodes to achieve consensus on the state of the blockchain ledger.
    >     * **QBFT**: QBFT (Quorum Byzantine Fault Tolerance) is a consensus algorithm designed for use in the Quorum blockchain platform, which extends Ethereum, providing Byzantine fault tolerance for private, permissive networks.
> * **Coinbase**: Address to pay mining rewards to. Can be any value in the genesis block (commonly set to 0x0000000000000000000000000000000000000000).
> * **Difficulty**: It determines the level of complexity or effort required for miners to add a new block to the blockchain.
> * **Version**: Version of the besu network, which you want to deploy.
> * **Reward Transfer**: Select where the mining reward will go.
    >     * **To Validator**: The reward will go to the validator who validated the block.
    >     * **To Mining beneficiary**: The reward will go to the particular address.
> * **Mining beneficiary Address**: Address of the account where block reward will go. only required if **To Mining beneficiary** is selected.
> * **Block Reward**: mining reward the beneficiary get on the successful validation of a block.
> * **Gas Free Network**: When enable you can create the transaction without any gas fee in the network. when disabled you need to define **Gas Limit**  and **Price**
> * **Gas Limit**: Total gas limit for all transactions in a block.
> * **Gas Price**: The gas price is the minimum amount of cryptocurrency you have to pay for each unit of gas consumed by the transaction.



After providing the details click on **Next step** to go to the **Bootnodes** page.


3. **Bootnodes:** 
Clicking on the card you will be landed on a page similar to the below image. In this section, we have to provide Bootnode related information.

    ![img](./images/besu/create-besu-step-3.png)

> *   **Bootnode name**: The name of the bootnode, it should be unique. You can't create any other node(rpc, validator or/and bootnode) with same name.
> *  **Add Bootnode**: To add more bootnode.
> *  **Trash Icon**: You can delete the node with the trash icon just above the **name** in top right position.

After providing the details click on **Next step** to go to the **Validator Nodes** page.

4. **Validator Nodes:** 
Clicking on the card you will be landed on a page similar to the below image. In this section, we have to provide validator related information.

    ![img](./images/besu/create-besu-step-4.png)

> *  **Validator Management Method**: The process of adding, removing, and maintaining validator nodes within a blockchain network.
    >     * **Block header Selection**: Existing validators propose and vote to add or remove validators using the QBFT JSON-RPC API methods.
    >     * **Smart Contract Selection**:  Use a smart contract to specify the validators used to propose and validate blocks.
> *   **Validator name**: The name of the validator node, it should be unique. You can't create any other node(rpc, validator or/and bootnode) with same name.
> *  **Add Validator**: To add more validator.
> *  **Trash Icon**: You can delete the node with the trash icon just above the **name** in top right position.

After providing the details click on **Next step** to go to the **RPC Nodes** page.

5. **RPC Nodes:** 
Clicking on the card you will be landed on a page similar to the below image. In this section, we have to provide rpc node related information.

    ![img](./images/besu/create-besu-step-5.png)

> *  **Add RPC Node**: To add more RPC node.
> *  **RPC Name**: The name of the RPC node, it should be unique. You can't create any other node(rpc, validator or/and bootnode) with same name.
> *  **Enable Public Endpoint**:
    >     * **HTTP**: Uses individual HTTP requests and responses for each call, similar to a RESTful API.
    >     * **ws**: WebSocket uses a persistent connection that allows the server to push data to the client.
> *  **Authentication Method**:
    >     * **API key**: Uses a key to authenticate the rpc calls.
    >     * **JWT**: use user name and password to generate a jwt token and use that to authenticate users.
> *  **JWT Username**: username for jwt authentication.
> *  **JWT Password**: password for jwt authentication.
> *  **Enable JSON-RPC API Method**: rpc method you want to enable for rpc.
> *  **Trash Icon**: You can delete the node with the trash icon just above the **name** in top right position.

After providing the details click on **Next step** to go to the **pre-minting** page.


6. **Pre-mining:** 
Clicking on the card you will be landed on a page similar to the below image. In this section, we have to provide pre minting related information.

    ![img](./images/besu/create-besu-step-6.png)
> *  **Add**: Add accounts address for pre minting tokens.
> *  **Account Address**: Address of the account for balance.
> *  **Account Balance**: Balance of that account.
> *  **Trash Icon**: You can delete the account and balance with the trash icon in the right.

After providing the details click on **Next step** to go to the **Configure cloud** page.

7. **Configure Cloud:** 
Clicking on the card you will be landed on a page similar to the below image. In this section, we have to provide Bootnode related information.

    ![img](./images/besu/create-besu-step-7.png)
> *  **Cloud Account**: Select the cloud account.
> *  **Region**: Select the region where you want to deploy network.
> *  **Deployment Type**: Select the deployment type for the network.
> *  **Total Worker Node Count**: number of worker node in the kubernetes cluster.
> *  **Worker Node Instance Type**: instance type of the worker node.
> *  **Worker Node Instance Type**: instance type of the worker node.

Click on the **Create** button to create network.

### **Add node to a network**

This section will guide you on how you can add a node to a network.


1. Select the network to which you want to add a node, and click on the network card [Ref.](./View_your_network_and_nodes.md). You will get to see similar to the below image.

    ![img](./images/viewNetwork.png)

2. Click on the **Actions** button on the top right, and select the **Add Node** option. You will get to see a web page similar to that provided below.

    ![img](./images/CoreumAddnode-1.png)

3. Fill in the details for the new node and click on the **Next** button. In this step, the cloud configuration and region will be prefilled according to the configuration of the network. Click on the **Create** button and it's done! 

    ![img](./images/CoreumAddnode-2.png)
 


### **Delete node in a network**

1. Select the network, in which you want to perform the delete node action, and click on the network card [Ref.](./View_your_network_and_nodes.md). You will get to see similar to the below image.

    ![img](./images/viewNetwork.png)

2. Click on the delete icon present alongside the node. A pop-up window will open for the confirmation, click on the **yes** button to confirm.
   
    ![img](./images/deleteNodeModal.png)

### **Delete a network**


1. Select the network you want to delete, and click on the network card[Ref.](./View_your_network_and_nodes.md). You will get to see similar to the below image.

    ![img](./images/viewNetwork.png)

2. Click on the *Actions* button on the top right, and select the **Delete Network** option. A confirmation window will open, click on the **Yes** button, attached to it.

    ![img](./images/deleteNetwork.png)

---
***NOTE*** It can take a few minutes to delete a network.

---

## Staking nodes


**NOTE** [Purchase](./subscriptions.md) a subscription before proceeding.



 1. [Create network](#create-a-network-2)
 2. [Update validator details](#update-validator-details)
 3. [Unbound token](#ubound-tokens)
 4. [Withdraw rewards](#withdraw-rewards)
 5. [Set rewards to a different wallet](#set-rewards-to-a-different-wallet)
 6. [Delete network](#delete-a-network-2)

### **Create a network**

This section will provide you detailed steps for creating a network of **Coreum**.

On the **Network Configuration** page you will be able to see different configuration cards for Coreum, which looks similar to the image provided below.

  ![img](./images/CoreumStakingNetworkConfiguration.png)

***NOTE:** These cards can be different for your case. Card configurations depend on your purchased subscription.*

---

You can Choose **Zeeve-Managed-Cloud** (Zeeve's managed hosting) for the infrastructure of your node or you can use your cloud account (AWS/DO) for the hosting of your node.

Choose the configuration you want. Click on the card and follow the steps accordingly.

1. **Network Info:** 
Clicking on the card you will be landed on a page similar to the below image. In this section, we have to provide network-related information for ex- Network Name, Network type, etc.

    ![img](./images/CoreumCreateStakingNetwork-1.png)

> *   **Name of Network**: To uniquely identify your network, this field requires a unique name for it. Unique over here is in terms of the account in which you are creating your network. In case you have created some network earlier, and now you are trying to create with the same name, then the [Zeeve](https://zeeve.io) platform won't allow you to create it.
> *  **Deployment Type**: Deployment type
> *  **Type Of Network**
>     *   **TestNet**: This will deploy your network on the network testnet. you can use this for your non-production needs like testing or demonstrations.
> *  **Workspace**: This represents the workspace in which the network will be added after successful creation.

After providing all the details correctly go to the next step by clicking on the **Next Step** button.

2. **Node Configuration:** 
In this section, you have to fill in the details of the nodes you want to add to your network.

    ![img](./images/CoreumCreateStakingNetwork-2.png)

> * **Node Name**: To identify your nodes, this field will be used. 
> * **Node MonikerId**: A custom human readable name for this node.
> * **Account MonikerId**: Account id.
> * **Validator Name**: The name which is visible on the Coreum Explorer. 
> * **Mnemonic Key**: bip39 mnemonic passphrase of your wallet. 
> * **Key Ring**: A passprase to access your private key. 
> * **Email**: Email will be used as a secret identity.
> * **Delegation Amount**: Amount which you want to delegate/stake. 
> * **Minimum Delegation Amount**: The minimum delegation amount and must be grater or equal min_self_delegation. 
> * **Commission Rate**: The initial commission rate percentage. 
> * **Commission Max. Rate**: The maximum commission rate percentage. 
> * **Commission Max. Change Rate**: The maximum commission change rate percentage (per day). 
> * **Website**: Website you want to be reflected in the. 
> * **Validator Identity**: The optional identity signature (ex. UPort or Keybase). 
> * **State Sync**: By enabling state sync your node will download data related to the head or near the head of the chain and verify the data. This leads to drastically shorter times for joining a network [Read more](https://docs.tendermint.com/v0.34/tendermint-core/state-sync.html).
> * **Username & Password**: Choose the username and password of your choice. These will be used as RPC API credentials.
> *  **Rpc Server**: RPC, which stands for "Remote Procedure Call," is a group of protocols and interfaces that let us talk to the blockchain system. Through the RPC interface, we can ask for information about the blockchain (such as block number, blocks, node connection, etc.) and send a request for a transaction. 
    >     * **HTTP**: Uses individual HTTP requests and responses for each call, similar to a RESTful API.
    >     * **ws**: WebSocket uses a persistent connection that allows the server to push data to the client.

After providing the details click on **Next step** to go to the last step.

3. **Cloud Configuration:**
This is the step for the configuration of the cloud for your nodes. This step can be different based on your selection of **Network configuration cards**
 
    1. [Zeeve Managed](#zeeve-managed)
    2. [BYOC - AWS](#byoc---aws)
    3. [BYOC - DO](#byoc---do)


---
#### Zeeve Managed
---

In the case of **Zeeve Managed**, you don't have to bother about anything, just select the region for the network by clicking on **Select Region**.

  ![img](./images/CoreumCreateStakingNetworkZeeveManaged.png)

> * **Region**: It indicates the region of cloud service. These regions are the geographic locations where your network instances are going to be hosted.

---
#### BYOC - AWS
---

In the case of **BYOC - AWS**, select the region for the network by clicking on **Select Region**, select the [AWS](./cloud_authorization.md) account you want to use by clicking on **Select Cloud Account**, also choose the instance type as your requirement by clicking on **Select Instance Type**.<br></br>

  ![img](./images/CoreumCreateStakingNetworkBYOC-AWS.png)

> * **Region**: It indicates the region of cloud service. These regions are the geographic locations where your network instances are going to be hosted. In the case of AWS, each of its regions has multiple, isolated locations known as Availability Zones. Amazon RDS provides you the ability to place resources, such as instances, and data in multiple locations. Resources aren't replicated across AWS Regions unless you do so specifically. [Ref.](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html)
> * **Cloud Account**: It represents the AWS cloud account that is going to be used for network creation. 
> *   **Type of Instance**: It defines the combination of CPU cores and memory. Choose the configuration which could handle loads of your network. This parameter is useful for scaling up the network. The type of Instances may vary from cloud to cloud.

---
#### BYOC - DO
---

In the case of **BYOC - DO**, select the region for the network by clicking on **Select Region**, select the [Digital Ocean](./cloud_authorization.md) account you want to use by clicking on **Select Cloud Account**, also choose the instance type as your requirement by clicking on **Select Instance Type**.<br></br>

  ![img](./images/CoreumCreateStakingNetworkBYOC-DO.png)

> * **Region**: It indicates the region of cloud service. These regions are the geographic locations where your network instances are going to be hosted. In the case of DigitalOcean, each of its regions has multiple, isolated locations known as Availability Zones. Digitial Ocean provides you the ability to place resources, such as instances, and data in multiple locations. Resources aren't replicated across it's Regions unless you do so specifically. [Ref.](https://docs.digitalocean.com/products/platform/availability-matrix/#available-datacenters)
> * **Cloud Account**: It represents the DO cloud account that is going to be used for network creation. 
> *   **Type of Instance**: It defines the combination of CPU cores and memory. Choose the configuration which could handle loads of your network. This parameter is useful for scaling up the network. The type of Instances may vary from cloud to cloud.


1. Click on the **Create** button. A pop-up window will appear similar to the below image, which ensures the successful creation of your network.

    ![img](./images/createNetworkSuccessModal.png)

5. Click on **continue** and you will be redirected to a page similar to the below image where you can see the nodes listed you've just added to the network.


### **Update Validator Details**

1. Find the Edit button on top right of the screen and click on it to edit and update the prefered validator detail. You will get to see similar to the below image.

    ***Step 01 :***

    * Validator Name
    > ![img](./images/coreum/update-validator-name.png)


    * Commission Rate
    > ![img](./images/coreum/update-commission-rate.png)


    * Email
    > ![img](./images/coreum/update-email.png)


    * Validator Identity
    > ![img](./images/coreum/update-validator-identity.png)

    
    ***Step 02 :***

    * Keyring is require in order to update the validator details.
    > ![img](./images/coreum/update-keyring.png)

### **Ubound tokens**

1. Click on the *Actions* button on the top right, and select the **Unbound Token** option.

    ![img](./images/coreum/validator-actions.png)

2. Enter the amount you want to unbound and the keyring, then click on Unbound button.
    
    > ![img](./images/coreum/action-unbound-token.png)


### **Withdraw rewards**

1. Click on the *Actions* button on the top right, and select the **Withdraw reward** option.

    ![img](./images/coreum/validator-actions.png)

2. Enter the keyring then click on Withdraw button.
    
    > ![img](./images/coreum/action-withdraw-reward.png)


### **Set rewards to a different wallet**

1. Click on the *Actions* button on the top right, and select the **Set rewards to a different wallet** option.

    ![img](./images/coreum/validator-actions.png)

2. Enter the wallet address and keyring then click on Set button.
    
    > ![img](./images/coreum/action-set-wallet-reward.png)

### **Delete a network**


1. Select the network you want to delete, and click on the network card. You will get to see similar to the below image.

    ![img](./images/coreum/validator-actions.png)

2. Click on the *Actions* button on the top right, and select the **Delete Network** option. A confirmation window will open, click on the **Yes** button, attached to it.

    ![img](./images/deleteNetwork.png)

---
***NOTE*** It can take a few minutes to delete a network.

---