## libuv native library library used by node

help node js to handle async oprations across diff os System

event loop
Worker thread loop
timers
async i/ko operation

v8 does not provide
fs operations
network socket handling
timers
general event loop for node js apis

node js needs something else ???
node js needs a another layer to coordinate runtime features

JS -> Node.js API -> c++ Binding -> libuv ->
libuv -> [event loop -> operating system] (vice versa)
libuv -> Thread Pool -> event loop -> Operating system
libuv -> Thread Pool -> Operating system
libuv -> Thread Pool -> Event loop -> JS

event loop ->
complete i/o operations
timers -> if some timers are in ready state 
panding callbacks
socket activity

thred pool ->
libuv provides a shared worker thread pool

this pool is used by only those operations that can not be handledefficiently

many file system operations
crypto graphic operations
compression related work

timers ->
libuv helps node js track those timers and imp -> determine when the timer is become elegable to execute
timer -> 5sec delay -> does not mean the Js speed on the main thread
runtime record the timer and  continue processing other task