
normal node js -> one main js thread

cluster module -> By starting multiple node js worker process

each and every worker process ->
its own node js runtime
its own v8 engine
its own event loop
its own main js thread
its own memory

Incoming Requests -> [primary Process , Shared server port] -> (Worker Process-1,2,3,4) -> (CPU Core -> 1,2,3,4)