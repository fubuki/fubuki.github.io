---
layout: post
title: "elasticsearch 載入順序"
date: 2015-10-24 23:16:32 +0800
comments: true
categories: ["elasticsearch"]
---


<!-- more -->

### Bootstrap

1. org.elasticsearch.bootstrap
2. init
3. bootstrapCLIParser
4. bootstrap
5. nodbuilder
6. node
7. node start


### Node
1. node load settings
2. node start
3. node load classes


### node loaded classes

        injector.getInstance(MappingUpdatedAction.class).setClient(client);
        injector.getInstance(IndicesService.class).start();
        injector.getInstance(IndexingMemoryController.class).start();
        injector.getInstance(IndicesClusterStateService.class).start();
        injector.getInstance(IndicesTTLService.class).start();
        injector.getInstance(SnapshotsService.class).start();
        injector.getInstance(SnapshotShardsService.class).start();
        injector.getInstance(TransportService.class).start();
        injector.getInstance(ClusterService.class).start();
        injector.getInstance(RoutingService.class).start();
        injector.getInstance(SearchService.class).start();
        injector.getInstance(MonitorService.class).start();
        injector.getInstance(RestController.class).start();