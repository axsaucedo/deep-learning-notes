
# Performance

GPUs are important.

GPUs are a powerful tool for training Deep Networks.

When it comes to speeding up training process, there are alternatives to GPUs.

## CPU Characteristics

CPUs comes with a cost - they require sophisticated control mechanisms in order to manage the flow of tasks.

CPU is also designed to perform tasks serially one after another rather than in parallel.

Parallelism can be achieved by building an unlimited number of cores directly in the CPU.

The cores are versatile but they need to be created with general purpose computing in mind.

Clock speeds haven't improved as much in the last few years, eventhough there has been minor improvements with CPU memory.

**A CPU is impractical for large scale deep nets.**

## Opportunity

### Vectors

We can implement deep nets using vectors and vector algebra.

Addition, dot product and transposes are operations that can be performed in parallel.

Each multiplication of the dot product can be performed in parallel, and the resulting products can be added together.

By using a parallel implementation, deeps nets can be trained much faster.

Parallelism implemented at a hardware level **is known as parallel processing**.

Parallelism at the software level is **parallel programming**.


### Parallel Processing

Implemented at hardware level

Can be broken down into:

* Shared memory
* Distributed computing

#### Shared memory options: GPU

Unlike CPUs, it has hundreds/thousands of cores.

Each GPU core is capable of general purpose computing

Any parallel task can be performed in GPUs

The most popular application of GPUs is the training process.

Deep learning community provides support to GPU with libraries, implementations, and an ecosystem fostered by nvidia.

**Disadvantage**: High power consumption. Bad for large scale deep nets.

#### Shared memory options: FPGA

Field programmable gate array (FPGA) is an alternative to GPU

They are highly configurable.

Originally used by electrical engineers to build mockups of different chip designs. That way engineers can test different solutions to a problem without having to redesign a chip each time.

They allow you to tweak the chip's function at the lowest level: **the logic gate**.

An FPGA can be tailored specifically for a deep network, allowing it to consume much less power than a GPU.

FPGAs can be used to run a deep net model and generate predictions.

This would be handy if you need to run a large scale Convoluted Neural Network across thousands of images per second.

**Disadvantages**: To properly configure an FPGA, an engineer would need highly specialized knowledge in circuit design.

#### Shared memory options: ASIC

Application Specific Integrated Circuit (ASIC) are highly specialized with designs built in at the hardware and integrated circuit level.

Once built they will perform for the task they were designed for, but unusable in any other application.

Compared to GPUs and FPGAs, ASICs tend to have the lowest consumption requirements.

Google has the google tensor processing unit, and nervana has another chip which both are ASICs

## Distributed Computing

Parallelism can also be implemented using distributed computing. 

Generally speaking, the 3 options for distributed computing are data parallelism, model parallelism and pipeline parallelism.

### Data parallelism

DP allows you to train different subsets of the data on different nodes in a cluster for each training pass

This is followed by parameter averaging, and replacement across the cluster.

### Model Parallelism

Model parallelism is used in tensor flow, where different portions of the model are trained in different devices in parallel.


### Pipeline Parallelism

It works like a production assembly line. 

Generally there will be a number of jobs to be completed.

Each task for a given job will be dedicated for a worker, ensuring that each worker is well utilized. 

When a worker finishes, it can move to do another task for another job.

## Parallel Programming 

A very well researched topic for years.

There are a set of advanced techniques (outside of scope of lesson)

Creating algorithms with parallelism in mind will allow to take full advantage of parallelism of the hardware.

Here are a few (from many) examples

### Model

The first method is to decompose the datamodel into chunks, where each chunk is needed to perform an instance of a task.

### Algorithm

Identify tasks that have dependencies and place them in a single group.

By creating multiple groups that have no dependencies on one another, you can process the final job in parallel by dividing up the groups

### Implementation

Implement threads and processes that handle different tasks or task groups

This method can be performed independently, but the performance benefits can be significant when combined in the 2nd method.
