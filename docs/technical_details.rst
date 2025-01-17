.. _technical_details:

Technical details
=================

We provide more information about the platform's internals for instructors and
contributors. Make sure you read :ref:`notebooks_howto` before going on!

The computing environments
--------------------------

The computing environments available via MyBinder are
`Docker containers <https://www.docker.com/resources/what-container>`_,
or "software capsules" that can be created, pushed and pulled online. We create
these containers using a few simple configuration files specifying the
software packages and python libraries we would like to used in OGGM-Edu.
These configurations files are found in this repository:
`<https://github.com/OGGM/binder>`_

MyBinder uses `repo2docker <https://repo2docker.readthedocs.io>`_ to build these
environments and stores them in a hidden database. Once built, they won't
be built again unless a new change is made to the ``OGGM/binder``
repository.

We use the same principle to build images that can be used by your own
JupyterHub deployment, if you have one.
These images are available `here <https://hub.docker.com/r/oggm/r2d>`_ and
form the base of the Binder environments. Their configuration files are found
in this repository: `<https://github.com/OGGM/r2d>`_.
We use these in :ref:`oggm_hub`.

The notebooks
-------------

The notebooks are developped collaboratively. We welcome your input and
contributions! You will find the directory with all notebooks (educational and
tutorials) on GitHub: `<https://github.com/OGGM/oggm-edu-notebooks>`_


This website
------------

The content of this website is written within the `Sphinx <http://sphinx-doc.org/>`_
framework and is hosted on `ReadTheDocs <https://readthedocs.org>`_.

.. _oggm_hub:

OGGM-Hub
--------

We also provide a dedicated OGGM JupyterLab running on our own server:
`OGGM-Hub <https://docs.oggm.org/en/stable/cloud.html#oggm-hub>`_.
The advantages of OGGM-Hub over Binder are:

- more resources for your students, faster launches
- user management: you can set passwords and user names at wish
- persistent sessions: work can be saved between sessions and log-ins (this is probably the main advantage of OGGM-Hub)

`hub.oggm.org <https://hub.oggm.org>`_ is only available to registered users (registration is free!),
but it won't work for an entire class. If you have a specific need for an
OGGM-hub service (e.g. for a one-week class or a workshop), please
:ref:`title_contact` to get access to `classroom.oggm.org <https://classroom.oggm.org>`_!
`classroom.oggm.org <https://classroom.oggm.org>`_ is a copy of
`hub.oggm.org <https://hub.oggm.org>`_, but with less resources allocated
to each user (good enough for a class though!).
