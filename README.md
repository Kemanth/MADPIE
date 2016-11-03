# Implementation of MADPIE algorithm in ns-3

## Course Code: CS822

## Assignment: #GP2

### Overview 

Maximum and Average queuing Delay with Proportional Integral controller Enhanced (MADPIE) [1] is an extension of PIE [2], that adds deterministic packet drops at controlled intervals. This repository provides an implementation of MADPIE in ns-3-dev, changeset 12328 [3].


### Simulating MADPIE

To simulate MADPIE algorithm, the attribute MADPIE must be set to true, as shown below:

`Config::SetDefault ("ns3::PieQueueDisc::MADPIE", BooleanValue (true));`

### MADPIE example

An example program for MADPIE has been provided in

`src/traffic-control/examples/pie-example.cc`

and should be executed as

`./waf --run "pie-example --queueDiscType=MADPIE"`


### References

[1] Kuhn, N., & Ros, D. (2016). Improving PIE's performance over high-delay paths. arXiv preprint arXiv:1602.00569.

[2] Pan, R., Natarajan, P., Piglione, C., Prabhu, M. S., Subramanian, V., Baker, F., & VerSteeg, B. (2013, July). PIE: A lightweight control scheme to address the bufferbloat problem. In High Performance Switching and Routing (HPSR), 2013 IEEE 14th International Conference on (pp. 148-155). IEEE.

[3] https://www.nsnam.org/ns-3-dev/
