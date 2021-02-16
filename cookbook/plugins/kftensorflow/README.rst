Executing Distributed TensorFlow training jobs on K8s
==========================================================
This plugin uses the Kubeflow TensorFlow Operator and provides an extremely simplified interface for executing distributed training using various TensorFlow backends.

Installation
------------

To use the flytekit distributed tensorflow plugin simply run the following:

.. prompt:: bash

   pip install flytekitplugins-kftensorflow==0.1.1


How to build your Dockerfile for TensorFlow on K8s
-----------------------------------------------

.. note::

    If using CPU for training then special dockerfile is NOT REQUIRED. If GPU or TPUs are required then, the dockerfile differs only in the driver setup. The following dockerfile is enabled for GPU accelerated training using CUDA


.. literalinclude:: ../../kftensorflow.Dockerfile
    :language: dockerfile
    :emphasize-lines: 1
    :linenos:
    :caption: Dockerfile for distributed tensorflow training is identical to the base dockerfile, except for using CUDA base
