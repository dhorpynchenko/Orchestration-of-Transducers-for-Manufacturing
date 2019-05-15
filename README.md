# Analysis of the paper "Synthesis of Orchestrations of Transducers for Manufacturing"
## Overview
## Implementation
As an example, there is jupyter notebook file under the the 'code' folder with orchestration algorithm for uni-transducers setting implementation.
### Setup
Requirements:
<ul>
<li>Python 3+</li>
<li>Graphviz library

1. Install python package using `pip install graphviz`
2. Install graphviz backend into your system https://graphviz.org/download/
    
    (Windows users must add to PATH `C:\Program Files (x86)\Graphviz2.38\bin`)
</li>
</ul>

### Domains
For running an algorithm on your domain you must represent it as a set of transducer's files.
There are few examples under 'domain' folder:
<ul>
<li>Manufacturing problem described in the paper

"The recipe specifies that parts are first cleaned and
then painted. Square parts are painted green, round parts
are painted yellow. (More generally, the colour of a part
could be determined by, e.g., an RFID tag attached to the
part, but this keeps things simple.) We have three manufacturing resources: a cleaning machine, and two painting machines, one that paints parts green and the other
paints them yellow."
</li>
<li>Automechanic setting

Following domain describes a service work done by automechanic. At first he must check the engine, then change filter and then pump wheels.
Wheel service can be done clockwise and counter-clockwise. Thus, as manufacturing resources we have 3 transducer's types: Engine Service, Filter Service and Wheels Service.
</li>
</ul>