
# Lead

## Overview :white_check_mark: 
```
root@vmi616941:~/joystream# yarn joystream-cli working-groups:overview -g=storageProviders
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/joystream-cli working-groups:overview -g=storageProviders
Initializing the query node connection (https://54.172.154.45.nip.io/query-node/server/graphql)...... done
Initializing the api connection (wss://54.172.154.45.nip.io/ws-rpc)...... done
Current Group: storageProviders

___________________ Group lead ___________________

 Member id:                    19
 Member handle:                yyagi
 Role account:                 j4RebjBfiGWUnBZiiHGwergmwfvU23iitYzkoXv37kbfnQpHv

____________________ Members _____________________

 Worker id     Member id     Member handle     Stake            Reward         Missed reward     Role account
 ───────────── ───────────── ───────────────── ──────────────── ────────────── ───────────────── ─────────────────── ────────
 1             19            yyagi             50.4279 kJOY     1.0000 JOY     8.6730 kJOY       j4Rebj...fnQpHv     ⭐ 🔑

_____________________ Legend _____________________

⭐ - Leader
🔑 - Role key available in CLI
Done in 15.82s.

```
## Import key :white_check_mark: 
```
root@vmi616941:~/joystream# /root/joystream/node_modules/.bin/joystream-cli account:import --backupFilePath=/root/keys/storage-role-key.json
Initializing the query node connection (https://54.172.154.45.nip.io/query-node/server/graphql)...... done
Initializing the api connection (wss://54.172.154.45.nip.io/ws-rpc)...... done
 New account name storage-role-key
? Current account password [hidden]
? Set new account's password [hidden]
? Confirm new account's password [hidden]

New account successfully created!
```

## Create Opening :white_check_mark:

```
root@vmi616941:~/joystream# yarn joystream-cli working-groups:createOpening -g=storageProviders
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/joystream-cli working-groups:createOpening -g=storageProviders
Initializing the query node connection (https://54.172.154.45.nip.io/query-node/server/graphql)...... done
Initializing the api connection (wss://54.172.154.45.nip.io/ws-rpc)...... done
Current Group: storageProviders
 Do you want to provide optional applicationDetails? Yes
 applicationDetails Exeperienced Storage Worker
 Do you want to provide optional expectedEndingTimestamp? No
 Do you want to provide optional hiringLimit? Yes
 hiringLimit 4
 Do you want to provide optional title? Yes
 title Exeperienced Storage Worker
 Do you want to provide optional shortDescription? No
 Do you want to provide optional description? No
 Do you want to provide optional applicationFormQuestions? No
 stakingPolicy.amount 4000
 stakingPolicy.unstakingPeriod 43200
 Do you want to provide optional rewardPerBlock? Yes
 rewardPerBlock 1
You need to increase your lead stake to 50.7612 kJOY in order to create a new opening.
{
    applicationDetails: "Exeperienced Storage Worker",
    hiringLimit: 4,
    title: "Exeperienced Storage Worker",
    stakingPolicy: {
        amount: 4000,
        unstakingPeriod: 43200
    },
    rewardPerBlock: 1
}
? Do you confirm the provided input? Yes
? Enter storage-role-key account password [hidden]

Sending storageWorkingGroup.addOpening extrinsic from storage-role-key...
Tx params: [
  [
    '0x18042a1b45786570657269656e6365642053746f7261676520576f726b65723a1b45786570657269656e6365642053746f7261676520576f726b6572',
    'Regular',
    { stakeAmount: '4,000', leavingUnstakingPeriod: '43,200' },
    '1'
  ]
]
? Tx fee of 145.9880 mJOY will be deduced from you account, do you confirm the transfer? Yes
 ›   Warning: Extrinsic failed! Extrinsic execution error: BelowMinimumStakes (Staking less than the lower bound.)
? Try again with remembered input? Yes
 Do you want to provide optional applicationDetails? Yes
 applicationDetails Exeperienced Storage Worker
 Do you want to provide optional expectedEndingTimestamp? No
 Do you want to provide optional hiringLimit? Yes
 hiringLimit 4
 Do you want to provide optional title? Yes
 title Exeperienced Storage Worker
 Do you want to provide optional shortDescription? Yes
 shortDescription Professional operation of a storage node.
 Do you want to provide optional description? No
 Do you want to provide optional applicationFormQuestions? No
 stakingPolicy.amount 3333333333333
 stakingPolicy.unstakingPeriod 43200
 Do you want to provide optional rewardPerBlock? Yes
 rewardPerBlock 1
You need to increase your lead stake to 50.7612 kJOY in order to create a new opening.
{
    applicationDetails: "Exeperienced Storage Worker",
    hiringLimit: 4,
    title: "Exeperienced Storage Worker",
    shortDescription: "Professional operation of a storage node.",
    stakingPolicy: {
        amount: 3333333333333,
        unstakingPeriod: 43200
    },
    rewardPerBlock: 1
}
? Do you confirm the provided input? Yes

Sending storageWorkingGroup.addOpening extrinsic from storage-role-key...
Tx params: [
  [
    '0x0a2950726f66657373696f6e616c206f7065726174696f6e206f6620612073746f72616765206e6f64652e18042a1b45786570657269656e6365642053746f7261676520576f726b65723a1b45786570657269656e6365642053746f7261676520576f726b6572',
    'Regular',
    {
      stakeAmount: '3,333,333,333,333',
      leavingUnstakingPeriod: '43,200'
    },
    '1'
  ]
]
? Tx fee of 160.9597 mJOY will be deduced from you account, do you confirm the transfer? Yes
Extrinsic successful!
Opening with id 2 successfully created!
2
Done in 495.45s.

```

## Increase the stake :white_check_mark: 

```
root@vmi616941:~/joystream# yarn joystream-cli working-groups:increaseStake 113340000000000
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/joystream-cli working-groups:increaseStake 3340000000000
Initializing the query node connection (https://54.172.154.45.nip.io/query-node/server/graphql)...... done
Initializing the api connection (wss://54.172.154.45.nip.io/ws-rpc)...... done
Current Group: storageProviders
? Enter storage-role-key account password [hidden]

Sending storageWorkingGroup.increaseStake extrinsic from storage-role-key...
Tx params: [ [ '1', '3,340,000,000,000' ] ]
? Tx fee of 98.9794 mJOY will be deduced from you account, do you confirm the transfer? Yes
Extrinsic successful!
Worker 1 stake has been increased by 334.0000 JOY
Done in 26.40s.
```


## Set "global" storage limits :white_check_mark: 

```
root@vmi616941:~/joystream# yarn storage-node leader:update-voucher-limits -s 2000000000000 -o 20000 -p ********* -k ~/keys/storage-role-key.json -u wss://54.172.154.45.nip.io/ws-rpc
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node leader:update-voucher-limits -s 2000000000000 -o 20000 -p ********* -k /root/keys/storage-role-key.json -u wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 22:15:52:1552 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 22:15:54:1554 info: Waiting for chain to be synced before proceeding.
2022-07-31 22:15:54:1554 info: Updating global storage bucket voucher limits....
2022-07-31 22:15:55:1555 debug: Sending storage.updateStorageBucketsVoucherMaxLimits extrinsic...
2022-07-31 22:16:00:160 debug: Extrinsic successful!
Done in 14.09s.
```

## Create Bucket :white_check_mark: 

```
root@vmi616941:~/joystream# yarn storage-node leader:create-bucket -a -i 1 -s 2000000000000 -n 20000 -u wss://54.172.154.45.nip.io/ws-rpc -p *********  -k /root/keys/storage-role-key.json
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node leader:create-bucket -a -i 1 -s 2000000000000 -n 20000 -u wss://54.172.154.45.nip.io/ws-rpc -p ********* -k /root/keys/storage-role-key.json
2022-07-31 15:14:44:1444 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 15:14:46:1446 info: Waiting for chain to be synced before proceeding.
2022-07-31 15:14:46:1446 info: Creating storage bucket...
2022-07-31 15:14:47:1447 debug: Sending storage.createStorageBucket extrinsic...
2022-07-31 15:14:48:1448 debug: Extrinsic successful!
```

## Disable Accepting new pags :white_check_mark:
```
root@vmi616941:~/joystream# yarn storage-node leader:update-bucket-status -i 5 -s off -u wss://54.172.154.45.nip.io/ws-rpc -p *********  -k ~/keys/storage-role-key.json
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node leader:update-bucket-status -i 5 -s off -u wss://54.172.154.45.nip.io/ws-rpc -p ********* -k /root/keys/storage-role-key.json
2022-07-31 22:12:07:127 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 22:12:09:129 info: Waiting for chain to be synced before proceeding.
2022-07-31 22:12:09:129 info: Updating the storage bucket status...
2022-07-31 22:12:10:1210 debug: Sending storage.updateStorageBucketStatus extrinsic...
2022-07-31 22:12:12:1212 debug: Extrinsic successful!
Done in 12.18s.
```

## Delete Bucket :white_check_mark:
```
root@vmi616941:~/joystream# yarn storage-node leader:delete-bucket -i 3 -u wss://54.172.154.45.nip.io/ws-rpc -p *********  -k ~/keys/storage-role-key.json
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node leader:delete-bucket -i 3 -u wss://54.172.154.45.nip.io/ws-rpc -p *********-k /root/keys/storage-role-key.json
2022-07-31 18:31:01:311 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 18:31:03:313 info: Waiting for chain to be synced before proceeding.
2022-07-31 18:31:03:313 info: Deleting storage bucket...
2022-07-31 18:31:04:314 debug: Sending storage.deleteStorageBucket extrinsic...
2022-07-31 18:31:06:316 debug: Extrinsic successful!
Done in 10.58s.
```



## Update/set the dynamic bag policy :white_check_mark:
```
root@vmi616941:~/joystream# yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 2 -u wss://54.172.154.45.nip.io/ws-rpc -p *********  -k ~/keys/storage-role-key.json
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node leader:update-dynamic-bag-policy -t Channel -n 2 -u wss://54.172.154.45.nip.io/ws-rpc -p ********* -k /root/keys/storage-role-key.json
2022-07-31 22:27:48:2748 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 22:27:50:2750 info: Waiting for chain to be synced before proceeding.
2022-07-31 22:27:50:2750 info: Update dynamic bag creation policy....
2022-07-31 22:27:51:2751 debug: Sending storage.updateNumberOfStorageBucketsInDynamicBagCreationPolicy extrinsic...
2022-07-31 22:27:54:2754 debug: Extrinsic successful!
Done in 12.10s.
```

## Update the bag limit :white_check_mark:
```
root@vmi616941:~/joystream# yarn storage-node leader:update-bag-limit -l 10 -u wss://54.172.154.45.nip.io/ws-rpc -p *********  -k ~/keys/storage-role-key.json
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node leader:update-bag-limit -l 10 -u wss://54.172.154.45.nip.io/ws-rpc -p ********* -k /root/keys/storage-role-key.json
2022-07-31 22:28:29:2829 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 22:28:31:2831 info: Waiting for chain to be synced before proceeding.
2022-07-31 22:28:31:2831 info: Update "Storage buckets per bag" number limit....
2022-07-31 22:28:32:2832 debug: Sending storage.updateStorageBucketsPerBagLimit extrinsic...
2022-07-31 22:28:36:2836 debug: Extrinsic successful!
Done in 13.26s.
```

## Enable Accepting new pags :white_check_mark:
```
root@vmi616941:~/joystream# yarn storage-node leader:update-bucket-status -i 5 -s on -u wss://54.172.154.45.nip.io/ws-rpc -p *********  -k ~/keys/storage-role-key.json
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node leader:update-bucket-status -i 5 -s on -u wss://54.172.154.45.nip.io/ws-rpc -p ********* -k /root/keys/storage-role-key.json
2022-07-31 22:13:20:1320 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 22:13:22:1322 info: Waiting for chain to be synced before proceeding.
2022-07-31 22:13:22:1322 info: Updating the storage bucket status...
2022-07-31 22:13:23:1323 debug: Sending storage.updateStorageBucketStatus extrinsic...
2022-07-31 22:13:30:1330 debug: Extrinsic successful!
Done in 16.48s.
```

# Worker

## Create a transaction keys :white_check_mark:

```
root@vmi616941:~/joystream# yarn joystream-cli account:create
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/joystream-cli account:create
Initializing the query node connection (https://54.172.154.45.nip.io/query-node/server/graphql)...... done
Initializing the api connection (wss://54.172.154.45.nip.io/ws-rpc)...... done
 New account name storage-transaction-key
New account memonic: retire own way pink warm warm speed basket field diary notable weekend
? Set new account's password [hidden]
? Confirm new account's password [hidden]
 ›   Warning: Using empty password is not recommended!

New account successfully created!
Done in 17.08s.
```


## Accept Bucket :white_check_mark:
```
root@vmi616941:~/joystream# yarn run storage-node operator:accept-invitation -i 5 -w 1 -t j4RebjBfiGWUnBZiiHGwergmwfvU23iitYzkoXv37kbfnQpHv -u wss://54.172.154.45.nip.io/ws-rpc -p *********  -k ~/keys/storage-role-key.json
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node operator:accept-invitation -i 5 -w 1 -t j4RebjBfiGWUnBZiiHGwergmwfvU23iitYzkoXv37kbfnQpHv -u wss://54.172.154.45.nip.io/ws-rpc -p ********* -k /root/keys/storage-role-key.json
2022-07-31 18:57:42:5742 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 18:57:44:5744 info: Waiting for chain to be synced before proceeding.
2022-07-31 18:57:44:5744 info: Accepting pending storage bucket invitation...
2022-07-31 18:57:45:5745 debug: Sending storage.acceptStorageBucketInvitation extrinsic...
2022-07-31 18:57:48:5748 debug: Extrinsic successful!
Done in 12.49s.
root@vmi616941:~/joystream# yarn run storage-node operator:set-metadata -i 5 -w 1 -j metadata.json -u wss://54.172.154.45.nip.io/ws-rpc -p *********  -k ~/keys/storage-role-key.json
yarn run v1.22.15
```

## Set Metadata :white_check_mark:

```
root@vmi616941:~/joystream# yarn run storage-node operator:set-metadata -i 5 -w 1 -j metadata.json -u wss://54.172.154.45.nip.io/ws-rpc -p ********* -k ~/keys/storage-role-key.json
yarn run v1.22.15
$ /root/joystream/node_modules/.bin/storage-node operator:set-metadata -i 5 -w 1 -j metadata.json -u wss://54.172.154.45.nip.io/ws-rpc -p ********* -k /root/keys/storage-role-key.json
2022-07-31 18:58:11:5811 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
2022-07-31 18:58:13:5813 info: Waiting for chain to be synced before proceeding.
2022-07-31 18:58:13:5813 info: Setting the storage operator metadata...
2022-07-31 18:58:14:5814 debug: Sending storage.setStorageOperatorMetadata extrinsic...
2022-07-31 18:58:18:5818 debug: Extrinsic successful!
Done in 12.53s.
```



## QN :white_check_mark:

```
oot@vmi616941:~/joystream# docker ps
CONTAINER ID   IMAGE                                           COMMAND                  CREATED         STATUS         PORTS                      NAMES
12375998a703   node:14                                         "docker-entrypoint.s…"   3 minutes ago   Up 3 minutes   0.0.0.0:8081->8081/tcp     graphql-server
b542d1732be3   node:14                                         "docker-entrypoint.s…"   3 minutes ago   Up 3 minutes                              processor
1d6b07832ad7   joystream/hydra-indexer-gateway:4.0.0-alpha.0   "docker-entrypoint.s…"   3 minutes ago   Up 3 minutes   0.0.0.0:4000->4000/tcp     hydra-indexer-gateway
47ca87dd2de0   joystream/hydra-indexer:v4.0.0-alpha.0          "docker-entrypoint.s…"   4 minutes ago   Up 4 minutes                              indexer
1f797cf23613   redis:6.0-alpine                                "docker-entrypoint.s…"   4 minutes ago   Up 4 minutes   127.0.0.1:6379->6379/tcp   redis
1db3fed438ec   postgres:12                                     "docker-entrypoint.s…"   8 minutes ago   Up 8 minutes   127.0.0.1:5432->5432/tcp   db
```

```
root@vmi616941:~/joystream# docker logs -f -n 100 processor
INFO: Last block: 1279  : 67654 blocks behind
INFO: Processing block: 0000001280-a1891, events count: 1
INFO: Processing block: 0000001281-02453, events count: 1
INFO: Last block: 1281  : 67652 blocks behind
INFO: Processing block: 0000001282-28937, events count: 1
INFO: Processing block: 0000001283-cb718, events count: 1
INFO: Processing block: 0000001284-199c4, events count: 1
INFO: Processing block: 0000001285-a1b10, events count: 1
INFO: Processing block: 0000001286-cf793, events count: 1
INFO: Last block: 1286  : 67648 blocks behind
INFO: Processing block: 0000001287-70191, events count: 1
INFO: Processing block: 0000001288-ef3a7, events count: 1
INFO: Processing block: 0000001289-497e7, events count: 1
INFO: Processing block: 0000001290-31aee, events count: 1
INFO: Processing block: 0000001291-fe549, events count: 1
INFO: Last block: 1291  : 67643 blocks behind
INFO: Processing block: 0000001292-cf5b5, events count: 1
INFO: Processing block: 0000001293-ac9d0, events count: 1
INFO: Processing block: 0000001294-57497, events count: 1
INFO: Processing block: 0000001295-00064, events count: 1
INFO: Processing block: 0000001296-5b180, events count: 1
INFO: Last block: 1296  : 67638 blocks behind
INFO: Processing block: 0000001297-f5bfa, events count: 1
INFO: Processing block: 0000001298-0b062, events count: 1
INFO: Processing block: 0000001299-73097, events count: 1
INFO: Processing block: 0000001300-5dbf9, events count: 1
INFO: Processing block: 0000001301-15ac8, events count: 1
INFO: Last block: 1301  : 67633 blocks behind
```


## Storage Node :white_check_mark:

```
root@vmi616941:~# curl https://joystream.yyagi.cloud/storage/api/v1/state/data
{"objectNumber":1,"totalSize":1880088,"tempDownloads":0,"tempDirSize":4096}
```


```
- Logs begin at Wed 2022-07-20 00:38:58 CEST, end at Mon 2022-08-01 17:27:35 CEST. --
Jul 31 18:59:18 vmi616941.contaboserver.net systemd[1]: Started Joystream Storage Node.
Jul 31 18:59:19 vmi616941.contaboserver.net yarn[3557083]: yarn run v1.22.15
Jul 31 18:59:19 vmi616941.contaboserver.net yarn[3557083]: $ /root/joystream/node_modules/.bin/storage-node server -u wss://54.172.154.45.nip.io/ws-rpc -w 1 -o 3333 -l /root/.joystream-storage/log/ -d />
Jul 31 18:59:24 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:24:5924 info: Initialized runtime connection: wss://54.172.154.45.nip.io/ws-rpc
Jul 31 18:59:26 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:26:5926 info: Waiting for chain to be synced before proceeding.
Jul 31 18:59:26 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:26:5926 info: Removing temp directory ...
Jul 31 18:59:26 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:26:5926 info: Creating temp directory ...
Jul 31 18:59:26 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:26:5926 debug: Local ID cache loaded.
Jul 31 18:59:27 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:27:5927 info: Query node endpoint set: https://54.172.154.45.nip.io/query-node/server/graphql
Jul 31 18:59:27 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:27:5927 info: Synchronization enabled.
Jul 31 18:59:27 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:27:5927 debug: Max file size runtime parameter: 10737418240
Jul 31 18:59:27 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:27:5927 info: Listening on http://localhost:3333
Jul 31 18:59:27 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 18:59:27:5927 info: Sync paused for 1 minute(s).
Jul 31 19:00:27 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:27:027 info: Resume syncing....
Jul 31 19:00:27 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:27:027 info: Started syncing...
Jul 31 19:00:27 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:27:027 debug: Query - storageBucketsConnection
Jul 31 19:00:28 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:28:028 debug: Sync - getting all storage buckets: offset = 0, limit = 1000
Jul 31 19:00:28 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:28:028 debug: Query - storageBagsConnection
Jul 31 19:00:29 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:29:029 debug: Query - storageDataObjectsConnection
Jul 31 19:00:29 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:29:029 debug: Sync - new objects: 0
Jul 31 19:00:29 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:29:029 debug: Sync - obsolete objects: 0
Jul 31 19:00:29 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:29:029 debug: Sync - started processing...
Jul 31 19:00:29 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:29:029 info: Sync ended.
Jul 31 19:00:29 vmi616941.contaboserver.net yarn[3557106]: 2022-07-31 19:00:29:029 info: Sync paused for 1 minute(s).
```
