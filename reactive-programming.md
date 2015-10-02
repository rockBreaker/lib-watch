# wtf is reactive programming
_WIP_
[gist source](https://gist.github.com/staltz/868e7e9bc2a7b8c1f754)

## Streams
A stream is a sequence of *on going events ordered in time.* 

####It can emit:

* A value (of some type)
* An error
* A _completed_ signal

####_Capturing_
Asynchronously capture these events using different emitter type functions. 

* Define a function which executes when:
  * A value is emitted
  * An error is emitted
  * 'completed' is emitted

Listening to the stream is called **subscribing**.
The functions we define are _observers_.
The stream is the subject being observed. 
> This is precisely the [Observer Design Pattern](https://en.wikipedia.org/wiki/Observer_pattern).

ASCII diagram:

```
--a---b-c---d---X---|->

a, b, c, d are emitted values
X is an error
| is the 'completed' signal
---> is the timeline
```




