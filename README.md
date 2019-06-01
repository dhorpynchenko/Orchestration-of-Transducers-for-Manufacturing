# Analysis of the paper "Synthesis of Orchestrations of Transducers for Manufacturing"
## Overview
From the abstract of the paper:

`"In this paper, we model manufacturing processes and facilities as transducers (automata with output). The problem of
whether a given manufacturing process can be realized by a
given set of manufacturing resources can then be stated as
an orchestration problem for transducers. We first consider
the conceptually simpler case of uni-transducers (transducers
with a single input and a single output port), and show that
synthesizing orchestrations for uni-transducers is EXPTIMEcomplete. Surprisingly, the complexity remains the same for
the more expressive multi-transducer case, where transducers
have multiple input and output ports and the orchestration is
in charge of dynamically connecting ports during execution."`

Presentation slides <a href="https://github.com/dhorpynchenko/Orchestration-of-Transducers-for-Manufacturing/blob/master/paper_presentation.pdf">paper_presentation.pdf</a>

## Implementation
As an example, there is <a href="https://github.com/dhorpynchenko/Orchestration-of-Transducers-for-Manufacturing/blob/master/code/orchertration.ipynb">jupyter notebook</a> file under the the 'code' folder with orchestration algorithm for uni-transducers setting implementation.

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
<li><a href="https://github.com/dhorpynchenko/Orchestration-of-Transducers-for-Manufacturing/tree/master/domains/paper_factory">Manufacturing problem described in the paper</a>

"The recipe specifies that parts are first cleaned and
then painted. Square parts are painted green, round parts
are painted yellow. (More generally, the colour of a part
could be determined by, e.g., an RFID tag attached to the
part, but this keeps things simple.) We have three manufacturing resources: a cleaning machine, and two painting machines, one that paints parts green and the other
paints them yellow."
</li>
<li><a href="https://github.com/dhorpynchenko/Orchestration-of-Transducers-for-Manufacturing/tree/master/domains/automechanic">Automechanic setting</a>

Following domain describes a service work done by automechanic. At first he must check the engine, then change filter and then pump wheels.
Wheel service can be done clockwise and counter-clockwise. Thus, as manufacturing resources we have 3 transducer's types: Engine Service, Filter Service and Wheels Service.
</li>
</ul>