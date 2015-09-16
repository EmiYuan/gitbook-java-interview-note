# 线程池中断策略
线程池中的线程容器已经放不下先的任务了，必须要有一个相应的策略来处理
##ThreadPoolExecutor内部的4个中断策略
###1. Abort
默认策略，中止新加入的任务
###2. CallerRuns
调用者运行，它既不会丢弃任务，也不会抛弃异常，它会把任务推回到调用者那里以缓解任务流
###3. Discard
默认放弃这个任务
###4. DiscardOldest
遗弃最老的的任务