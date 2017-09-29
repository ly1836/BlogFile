---
title: test
date: 2017-09-27 15:26:44
tags: [java,karaf]
---

js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:512:31)
    at Promise._settlePromise (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:569:18)
    at Promise._settlePromise0 (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:614:10)
    <!--more-->
    at Promise._settlePromises (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:693:18)
    at Async._drainQueue (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:133:16)
    at Async._drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:143:10)
    at Immediate.Async.drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:17:14)
    at runCallback (timers.js:781:20)
ERROR Theme config load failed.
ERROR Process failed: _config.yml
YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key at line 690, column 3:
      three_waves
      ^
    at generateError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:165:10)

    at throwError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:171:9)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1046:9)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1062:11)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readDocument (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1492:3)
    at loadDocuments (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1548:5)
    at Object.load (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1569:19)
    at Hexo.yamlHelper (D:\gitHub\Bolg-Data\node_modules\hexo\lib\plugins\renderer\yaml.js:7:15)
    at Hexo.tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Hexo.<anonymous> (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\method.js:15:34)
    at D:\gitHub\Bolg-Data\node_modules\hexo\lib\hexo\render.js:61:21
    at tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:512:31)
    at Promise._settlePromise (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:569:18)
    at Promise._settlePromise0 (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:614:10)
    at Promise._settlePromises (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:693:18)
    at Async._drainQueue (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:133:16)
    at Async._drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:143:10)
    at Immediate.Async.drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:17:14)
    at runCallback (timers.js:781:20)
INFO  Bye!

终止批处理操作吗(Y/N)? Y
PS D:\gitHub\Bolg-Data> hexo clean
INFO  Deleted database.
PS D:\gitHub\Bolg-Data> hexo server
INFO  Start processing
ERROR Theme config load failed.
ERROR Process failed: _config.yml
YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key at line 690, column 3:
      # three_waves
      ^
    at generateError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:165:10)
    at throwError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:171:9)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1046:9)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1062:11)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readDocument (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1492:3)
    at loadDocuments (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1548:5)
    at Object.load (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1569:19)
    at Hexo.yamlHelper (D:\gitHub\Bolg-Data\node_modules\hexo\lib\plugins\renderer\yaml.js:7:15)
    at Hexo.tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Hexo.<anonymous> (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\method.js:15:34)
    at D:\gitHub\Bolg-Data\node_modules\hexo\lib\hexo\render.js:61:21
    at tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:512:31)
    at Promise._settlePromise (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:569:18)
    at Promise._settlePromise0 (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:614:10)
    at Promise._settlePromises (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:693:18)
    at Async._drainQueue (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:133:16)
    at Async._drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:143:10)
    at Immediate.Async.drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:17:14)
    at runCallback (timers.js:781:20)
INFO  Hexo is running at http://localhost:4000/. Press Ctrl+C to stop.
ERROR Theme config load failed.
ERROR Process failed: _config.yml
YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key at line 690, column 3:
      # three_waves
      ^
    at generateError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:165:10)
    at throwError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:171:9)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1046:9)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1062:11)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readDocument (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1492:3)
    at loadDocuments (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1548:5)
    at Object.load (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1569:19)
    at Hexo.yamlHelper (D:\gitHub\Bolg-Data\node_modules\hexo\lib\plugins\renderer\yaml.js:7:15)
    at Hexo.tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Hexo.<anonymous> (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\method.js:15:34)
    at D:\gitHub\Bolg-Data\node_modules\hexo\lib\hexo\render.js:61:21
    at tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:512:31)
    at Promise._settlePromise (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:569:18)
    at Promise._settlePromise0 (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:614:10)
    at Promise._settlePromises (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:693:18)
    at Async._drainQueue (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:133:16)
    at Async._drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:143:10)
    at Immediate.Async.drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:17:14)
    at runCallback (timers.js:781:20)
ERROR Theme config load failed.
ERROR Process failed: _config.yml
YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key at line 690, column 3:
      # three_waves
      ^
    at generateError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:165:10)
    at throwError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:171:9)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1046:9)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1062:11)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readDocument (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1492:3)
    at loadDocuments (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1548:5)
    at Object.load (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1569:19)
    at Hexo.yamlHelper (D:\gitHub\Bolg-Data\node_modules\hexo\lib\plugins\renderer\yaml.js:7:15)
    at Hexo.tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Hexo.<anonymous> (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\method.js:15:34)
    at D:\gitHub\Bolg-Data\node_modules\hexo\lib\hexo\render.js:61:21
    at tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:512:31)
    at Promise._settlePromise (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:569:18)
    at Promise._settlePromise0 (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:614:10)
    at Promise._settlePromises (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:693:18)
    at Async._drainQueue (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:133:16)
    at Async._drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:143:10)
    at Immediate.Async.drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:17:14)
    at runCallback (timers.js:781:20)
ERROR Theme config load failed.
ERROR Process failed: _config.yml
YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key at line 690, column 3:
      # three_waves
      ^
    at generateError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:165:10)
    at throwError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:171:9)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1046:9)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1062:11)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readDocument (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1492:3)
    at loadDocuments (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1548:5)
    at Object.load (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1569:19)
    at Hexo.yamlHelper (D:\gitHub\Bolg-Data\node_modules\hexo\lib\plugins\renderer\yaml.js:7:15)
    at Hexo.tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Hexo.<anonymous> (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\method.js:15:34)
    at D:\gitHub\Bolg-Data\node_modules\hexo\lib\hexo\render.js:61:21
    at tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:512:31)
    at Promise._settlePromise (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:569:18)
    at Promise._settlePromise0 (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:614:10)
    at Promise._settlePromises (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:693:18)
    at Async._drainQueue (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:133:16)
    at Async._drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:143:10)
    at Immediate.Async.drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:17:14)
    at runCallback (timers.js:781:20)
ERROR Theme config load failed.
ERROR Process failed: _config.yml
YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key at line 690, column 3:
      # three_waves
      ^
    at generateError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:165:10)
    at throwError (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:171:9)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1046:9)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readBlockMapping (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1062:11)
    at composeNode (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1332:12)
    at readDocument (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1492:3)
    at loadDocuments (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1548:5)
    at Object.load (D:\gitHub\Bolg-Data\node_modules\js-yaml\lib\js-yaml\loader.js:1569:19)
    at Hexo.yamlHelper (D:\gitHub\Bolg-Data\node_modules\hexo\lib\plugins\renderer\yaml.js:7:15)
    at Hexo.tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Hexo.<anonymous> (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\method.js:15:34)
    at D:\gitHub\Bolg-Data\node_modules\hexo\lib\hexo\render.js:61:21
    at tryCatcher (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:512:31)
    at Promise._settlePromise (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:569:18)
    at Promise._settlePromise0 (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:614:10)
    at Promise._settlePromises (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\promise.js:693:18)
    at Async._drainQueue (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:133:16)
    at Async._drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:143:10)
    at Immediate.Async.drainQueues (D:\gitHub\Bolg-Data\node_modules\bluebird\js\release\async.js:17:14)