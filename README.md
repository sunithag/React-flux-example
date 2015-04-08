# React-flux-example

new kind of architecture that complements React and the concept of Unidirectional Data Flow.

Controller view is basically root component (stateful)

Facebook does provide a repo that includes a Dispatcher library. 
The dispatcher is a sort of global pub/sub handler that broadcasts payloads to registered callbacks.

A typical Flux architecture will leverage this Dispatcher library, 
along with NodeJS’s EventEmitter module in order to set up an event system that helps manage 
an applications state.

<img src="https://cask.scotch.io/2014/10/V70cSEC.png">

Actions - Helper methods that facilitate passing data to the dispatcher

Dispatcher - Receives actions and broadcasts payloads to registered callbacks.
Dispatcher acts as traffic controller for the whole thing

Stores - Containers for application state & logic that have callbacks registered to the dispatcher.
data layer that updates whenever you have an action.
Registers events with dispatcher and executes them

controller views - React components that grab state from store and pass it deown via props to the child components
