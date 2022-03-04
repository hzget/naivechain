# p2p logs

Suppose there're 3 nodes. And the peer relatinships are:

node1(172.20.0.2) <---> node2(172.20.0.3) <---> node3(172.20.0.4)

## create a block for node1 from http endpoint

```
naivechain-node1-1  | block added: {"index":2,"previousHash":"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f","timestamp":1646404048.741,"data":"Some data to the first block 2nd mine","hash":"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e"}
naivechain-node1-1  | broadcast: 
naivechain-node1-1  |  ==> 172.20.0.3:42798 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
naivechain-node1-1  | <==  172.20.0.3:42798 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
naivechain-node1-1  | received blockchain is not longer than current blockchain. Do nothing

naivechain-node2-1  | <==  172.20.0.2:6001 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
naivechain-node2-1  | blockchain possibly behind. We got: 1 Peer got: 2
naivechain-node2-1  | We can append the received block to our chain
naivechain-node2-1  | broadcast: 
naivechain-node2-1  |  ==> 172.20.0.2:6001 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
```

## node3 joins in the network

```
naivechain-node3-1  | listening websocket p2p port on: 6001
naivechain-node3-1  | Listening http on port: 3001
naivechain-node3-1  |  ==> 172.20.0.3:6001 (QUERY_LATEST): {"type":0}
naivechain-node3-1  | <==  172.20.0.3:6001 (QUERY_LATEST): {"type":0}
naivechain-node3-1  |  ==> 172.20.0.3:6001 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":0,\"previousHash\":\"0\",\"timestamp\":1465154705,\"data\":\"my genesis block!!\",\"hash\":\"816534932c2b7154836da6afc367695e6337db8a921823784c14378abed4f7d7\"}]"}
naivechain-node3-1  | <==  172.20.0.3:6001 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
naivechain-node3-1  | blockchain possibly behind. We got: 0 Peer got: 2
naivechain-node3-1  | We have to query the chain from our peer
naivechain-node3-1  | broadcast: 
naivechain-node3-1  |  ==> 172.20.0.3:6001 (QUERY_ALL): {"type":1}
naivechain-node3-1  | <==  172.20.0.3:6001 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":0,\"previousHash\":\"0\",\"timestamp\":1465154705,\"data\":\"my genesis block!!\",\"hash\":\"816534932c2b7154836da6afc367695e6337db8a921823784c14378abed4f7d7\"},{\"index\":1,\"previousHash\":\"816534932c2b7154836da6afc367695e6337db8a921823784c14378abed4f7d7\",\"timestamp\":1646404022.294,\"data\":\"Some data to the first block\",\"hash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\"},{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
naivechain-node3-1  | blockchain possibly behind. We got: 0 Peer got: 2
naivechain-node3-1  | Received blockchain is longer than current blockchain
naivechain-node3-1  | Received blockchain is valid. Replacing current blockchain with received blockchain
naivechain-node3-1  | broadcast: 
naivechain-node3-1  |  ==> 172.20.0.3:6001 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}


naivechain-node2-1  |  ==> 172.20.0.4:48718 (QUERY_LATEST): {"type":0}
naivechain-node2-1  | <==  172.20.0.4:48718 (QUERY_LATEST): {"type":0}
naivechain-node2-1  |  ==> 172.20.0.4:48718 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
naivechain-node2-1  | <==  172.20.0.4:48718 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":0,\"previousHash\":\"0\",\"timestamp\":1465154705,\"data\":\"my genesis block!!\",\"hash\":\"816534932c2b7154836da6afc367695e6337db8a921823784c14378abed4f7d7\"}]"}
naivechain-node2-1  | received blockchain is not longer than current blockchain. Do nothing
naivechain-node2-1  | <==  172.20.0.4:48718 (QUERY_ALL): {"type":1}
naivechain-node2-1  |  ==> 172.20.0.4:48718 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":0,\"previousHash\":\"0\",\"timestamp\":1465154705,\"data\":\"my genesis block!!\",\"hash\":\"816534932c2b7154836da6afc367695e6337db8a921823784c14378abed4f7d7\"},{\"index\":1,\"previousHash\":\"816534932c2b7154836da6afc367695e6337db8a921823784c14378abed4f7d7\",\"timestamp\":1646404022.294,\"data\":\"Some data to the first block\",\"hash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\"},{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
naivechain-node2-1  | <==  172.20.0.4:48718 (RESPONSE_BLOCKCHAIN): {"type":2,"data":"[{\"index\":2,\"previousHash\":\"d44e6a35d9ffe4691fb353fc5bd6be989b2e963cb4c13a10a156f8867d0e225f\",\"timestamp\":1646404048.741,\"data\":\"Some data to the first block 2nd mine\",\"hash\":\"34f8b59dc3549abd5317a5a93e5382b2ebdf99fcb7e1043f06905480550c125e\"}]"}
naivechain-node2-1  | received blockchain is not longer than current blockchain. Do nothing
```

