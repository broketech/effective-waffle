Effective waffle rough/notes
----------------------------

```
diff -r V2TRUMP/src/bitcoinrpc.cpp V2TRUMP_test/src/bitcoinrpc.cpp
953c953
<     if (strMethod != "getwork" && strMethod != "getblocktemplate")
---
>     //if (strMethod != "getwork" && strMethod != "getblocktemplate")
diff -r V2TRUMP/src/leveldb/Makefile V2TRUMP_test/src/leveldb/Makefile
9c9
< OPT ?= -O2 -DNDEBUG       # (A) Production use (optimized mode)
---
> OPT ?= -O2 -fPIC -DNDEBUG       # (A) Production use (optimized mode)
diff -r V2TRUMP/src/rpcmining.cpp V2TRUMP_test/src/rpcmining.cpp
118,119c118,119
<     if (pindexBest->nHeight >= SAFETY_NET)
<         throw JSONRPCError(RPC_MISC_ERROR, "No more PoW blocks");
---
>   //  if (pindexBest->nHeight >= SAFETY_NET)
>   //      throw JSONRPCError(RPC_MISC_ERROR, "No more PoW blocks");
249,250c249,250
<    // if (IsInitialBlockDownload())
<    //     throw JSONRPCError(RPC_CLIENT_IN_INITIAL_DOWNLOAD, "TrumpCoin is downloading blocks...");
---
>     if (IsInitialBlockDownload())
>         throw JSONRPCError(RPC_CLIENT_IN_INITIAL_DOWNLOAD, "TrumpCoin is downloading blocks...");
252,253c252,253
<     if (pindexBest->nHeight >= SAFETY_NET)
<         throw JSONRPCError(RPC_MISC_ERROR, "No more PoW blocks");
---
>    // if (pindexBest->nHeight >= SAFETY_NET)
>      //   throw JSONRPCError(RPC_MISC_ERROR, "No more PoW blocks");
393,394c393,394
<     //if (IsInitialBlockDownload())
<     //    throw JSONRPCError(RPC_CLIENT_IN_INITIAL_DOWNLOAD, "TrumpCoin is downloading blocks...");
---
>     if (IsInitialBlockDownload())
>         throw JSONRPCError(RPC_CLIENT_IN_INITIAL_DOWNLOAD, "TrumpCoin is downloading blocks...");
396,397c396,397
<     if (pindexBest->nHeight >= SAFETY_NET)
<         throw JSONRPCError(RPC_MISC_ERROR, "No more PoW blocks");
---
>     //if (pindexBest->nHeight >= SAFETY_NET)
>     //    throw JSONRPCError(RPC_MISC_ERROR, "No more PoW blocks");
522c522,524
<     try {
---
>     try {
> //printf("%x\n",ssBlock);
> //printf("%x\n",block);
```
