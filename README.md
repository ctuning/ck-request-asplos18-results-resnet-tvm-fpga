[![logo](https://github.com/ctuning/ck-guide-images/blob/master/logo-powered-by-ck.png)](https://github.com/ctuning/ck)

This repository contains raw experimental results in [the CK format](https://github.com/ctuning/ck)
for the [image classification workflow](https://github.com/ctuning/ck-request-asplos18-resnet-tvm-fpga)
from the [ReQuEST tournament at ASPLOS'18](http://cknowledge.org/request-cfp-asplos2018.html) 
on reproducible SW/HW co-design of deep learning (speed, accuracy, energy, costs).
The [live ReQuEST scoreboard](http://cKnowledge.org/request-results) shows a subset of these results.

## Citations

* [ACM paper](https://doi.org/10.1145/3229762.3229766)
* [ACM artifact](https://doi.org/10.1145/3229772)

* [arXiv ReQuEST intro](https://arxiv.org/abs/1801.06378)

## Installation

### Minimal CK installation

The minimal installation requires:

* Python 2.7 or 3.3+ (limitation is mainly due to unitests)
* Git command line client.

You can install CK in your local user space as follows:

```
$ git clone http://github.com/ctuning/ck
$ export PATH=$PWD/ck/bin:$PATH
$ export PYTHONPATH=$PWD/ck:$PYTHONPATH
```

You can also install CK via PIP with sudo to avoid setting up environment variables yourself:

```
$ sudo pip install ck
```

### Install this CK repository and dependencies

```
$ ck pull repo:ck-request-asplos18-results-resnet-tvm-fpga
```

### List available experiments
```
$ ck ls ck-request-asplos18-results-resnet-tvm-fpga:experiment:*
```

### Replay experiment

```
$ ck replay experiment:{name from above list}
```

Note that CK will try to automatically rebuild experimental setup 
by detecting already installed software dependencies and installing missing ones
using shared [CK packages](https://github.com/ctuning/ck/wiki/Shared-packages).

If you want to have a software setup as close to the original one 
as possible, install packages before running replay as described in 
[the ReadMe](https://github.com/ctuning/ck-request-asplos18-resnet-tvm-fpga)
of the related CK workflow.

### Start dashboard to visualize/compare results

```
$ ck dashboard request.asplos18 --results=ck-request-asplos18-results-resnet-tvm-fpga
```

### See the live scoreboard

[Link](http://cKnowledge.org/request-results)


## Further discussions

* [Collective Knowledge mailing list](http://groups.google.com/group/collective-knowledge)
* [Artifact evaluation mailing list](http://groups.google.com/group/artifact-evaluation)
