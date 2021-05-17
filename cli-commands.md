This commands are useable with the cli as well as the wallet (console)  

`getblockchaininfo` => get chain info  
`getblocktemplate` => view the template for blocks  
`getaddednodeinfo` => see the connected nodes  
`getbestblockhash` => hash  
`getblockcount` => get the blocks  
`getchaintxstats` => TX infos  
`getdifficulty` => see the current difficulty to mine blocks  
`getmemoryinfo` => memory stats  
`getmempoolinfo` => pooled mem info  
`getnettotals` => stats about the net  
`getnetworkhashps` => overall hashing stats  
`getmininginfo` => miner infos, stats  
`getnodeaddresses` => find potential new nodes in the network  

#### fun with the gothchain
Verify the genesis block:  
`gothcoin-cli getblockhash 0` => `629ad0c776b91ca669e53a1172e7e2cf9ea71fe47f9b9b798c4d25159e988abe`  

Now let's get the raw block info:  
`gothcoin-cli getblock 629ad0c776b91ca669e53a1172e7e2cf9ea71fe47f9b9b798c4d25159e988abe 2`  

Here you find the `hex` part:  
`"hex": "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff3d04ffff001d0104354174207468652064617465206f66204d6179203135203230323120476f7468206465636c6172656420496e646570656e64656e6365ffffffff0100026489010000004341044cbb204252e19f8ce082cfd5643f269d73bf10f7da75bf7803c5a8c41f3956dc051a44402b1fa925e0c8cf9466386b6b7fb42fe38ea2eb938f3dff4214b89c67ac00000000"`  

Curios what's inside? Let's look with ASCII:  
`echo 01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff3d04ffff001d0104354174207468652064617465206f66204d6179203135203230323120476f7468206465636c6172656420496e646570656e64656e6365ffffffff0100026489010000004341044cbb204252e19f8ce082cfd5643f269d73bf10f7da75bf7803c5a8c41f3956dc051a44402b1fa925e0c8cf9466386b6b7fb42fe38ea2eb938f3dff4214b89c67ac00000000 | xxd -r -p`  
����=��5At the date of May 15 2021 Goth declared Independence����d�CAL� BR៌���d?&�s���u�xŨ�9V�D@+�%��ϔf8kk�/㎢듏=�B��g�
