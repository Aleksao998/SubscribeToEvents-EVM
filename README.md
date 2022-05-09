# SubscribeToEvents-EVM

This repo is for subscribing to contract events

## How to use it

1. Deploy contract (You can use events.sol or any other)
   Option 1: Remix (https://remix.ethereum.org/)
   Option 2: https://github.com/Aleksao998/DeployingAndCallingContract-EVM
 
2. Add network and account detail
  ```
  client, err := ethclient.Dial("ws://localhost:10002/ws") <NETWORK>
	if err != nil {
		log.Fatal(err)
	}

	contractAddress := common.HexToAddress("0xBD2b7892160573102Cd99eFdBabCB02babacbF72") <CONTRACT ADDRESS>
	query := ethereum.FilterQuery{
		Addresses: []common.Address{contractAddress},
	}
  ```
  
  3. go run main.go 
  4. Wait for events :)

