# workerdrop-scripts-public


# How to see my worker balances :
## Option A :  with VM and iexec-sdk ?

- In the VM desktop, enter the folder iExec
- Right click. "Open in Teminal"
- To see your RLC balance 
```
iexec wallet show --chain mainnet
```
- To see RLC deposit balance and rewards 
```
iexec account show --chain mainnet
```

You will notice 2 differents lines for the account balance. ‘Stake’ and ‘Locked’.

Stake balance can be withdrawn from marketplace and received as ERC20 RLC as you know it. This ‘Stake’ balance can be used either to stake or to pay for executions and is the balance increased when you make a deposit.

When workers place their stake to execute a task, ‘Stake’ balance decreases and ‘Locked’ balance increases accordingly.

These funds are locked until the work order is complete. When the work order is completed (and PoCo consensus is achieved), ‘Locked ’balance of the user is seized and the stake balance of contributors (workers) is increased, according to smart contract rewards distributions rules.

## Option B :How to see my worker balances with etherscan ?
 To see your RLC balance . As usual in etherescan 

To see RLC deposit balance and rewards :
https://etherscan.io/address/0x0d5ef019ca4c5cc413ee892ced89d7107c5f424d#readContract

scroll down to :
7. checkBalance

- Put your worker address in _owner (address)

and click : Query

## Option C: How to see my worker balances with iExec Account interface ?

To see your balance using the Account interface:

* Go to the [marketplace](https://market.iex.ec/)
* In Metamask (latest version only), click on 'Expand View'
* Click on ‘Import wallet’
* Select the type ‘JSON file’
* Type your password
* Click on ‘IMPORT’

Now you can click on ‘Account’ to manage your account.


# How to withdraw my rewards ? 

Just click on "Stop worker" Icon in the desktop VM. It will ask you to withdraw if you have any rewards or balances. See iexec-sdk withdraw code used [here](https://github.com/iExecBlockchainComputing/workerdrop-scripts-public/blob/master/stop-worker.sh#L33) 
