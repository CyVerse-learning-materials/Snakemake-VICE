|CyVerse logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

Workflow Management Using Snakemake
===================================

In this webinar you'll learn about `snakemake <https://snakemake.readthedocs.io/en/stable/>`_, a workflow management system consisting of a text-based workflow specification language and a scalable execution environment. A workflow management system (WMS) is a piece of software that sets up, performs and monitors a defined sequence of computational tasks (i.e. "a workflow"). Snakemake is a WMS that was developed in the bioinformatics community, and as such it has some features that make it particularly well suited for creating reproducible and scalable data analyses. 

Topics covered:
---------------
- Snakemake syntax and basics
- Visualization and workflow management
- Example RNAseq workflow of MRSA


.. Note:: 
  
  Special Thanks to instructors at `NBIS <https://nbis.se/>`_ (ELIXIR-SE) for the tutorial used here. This tutorial is one of 6-part course on **Tools for reproducible research**. Read more `here <https://www.scilifelab.se/events/tools-for-reproducible-research-4/>`_

- See Snakemake Slides `here <https://slides.com/johanneskoester/snakemake-tutorial#/>`_ and `pdf <https://github.com/CyVerse-learning-materials/Snakemake-VICE/blob/master/snakemake.pdf>`_.
----

Prerequisites
-------------

Downloads, access, and services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this tutorial you will need access to the following services/software*

	.. list-table::
	    :header-rows: 1

	    * - Prerequisite
	      - Preparation/Notes
	      - Link/Download
	    * - CyVerse account
	      - You will need a CyVerse account to complete this exercise
	      - `Register <https://user.cyverse.org/>`_
      * - familiarity with the terminal
        - `UNIX intro <https://astrobiomike.github.io/unix/>`_
        - Python and R knowledge would be beneficial

----

Platform(s)
~~~~~~~~~~~

*We will use the following CyVerse platform(s):*

.. list-table::
    :header-rows: 1

    * - Platform
      - Interface
      - Link
      - Platform Documentation
      - Learning Center Docs
    * - Discovery Environment
      - Web/Point-and-click
      - `Discovery Environment <https://de.cyverse.org/de/>`_
      - `DE Manual <https://wiki.cyverse.org/wiki/display/DEmanual/Table+of+Contents>`_
      - `Guide <https://learning.cyverse.org/projects/discovery-environment-guide/en/latest/>`__

----

----

*Quick Launch Snakemake-VICE Jupyter lab app*
---------------------------------------------

- Right-Click the button below and login to CyVerse Discovery Environment for a quick launch of Snakemake-VICE Jupyter-lab app.
  
  |smake-vice|_

*OR search within Discovery Environment*
----------------------------------------

1. Login to the |discovery_enviornment|.

2. CLick on "Apps" tab in the Discovery Enviornment and search for "snakemake".
  
3. Under “Analysis Name” leave the defaults or make any desired notes.

   .. Note::

	    The app comes pre-loaded with required software required for performing RNAseq analysis.

4. Under "Resource Requirements" request resources as needed or leave for defaults 

5. Click **Launch Analysis**. You will receive a notification that the job has been submitted and running in your notification tab.

.. Note::

  You will be notified when the analysis has finished successfully.

6. Click on the "Analyses" button to display the dashboard of your analyses. Click on your anlaysis name to
navigate to that analysis folder in your data store. 

7. Click `here <https://nbis-reproducible-research.readthedocs.io/en/devel/snakemake/>`_ for the tutorial.

----

*RNA-seq analysis of MRSA Workflow*
-----------------------------------

- Clone RNAseq Snakemake tutorial repository

.. code::  
  
  git clone https://github.com/NBISweden/workshop-reproducible-research.git
  
  cd workshop-reproducible-research/docker/
  
  git checkout devel
  
  ls
  
- Generate rulegraph  
.. code::  
  
  snakemake --rulegraph | dot -Tpng > rulegraph_mrsa.png

- Dry-Run RNAseq Snakefile   
.. code::  
  
  snakemake -n

- Run RNAseq Snakefile   
.. code::  
  
  snakemake --cores 8

----

.. Note:: 
  
  Here we used the package snakemake-minimal. This is a slimmed down version that lack some features, in particular relating to cloud computing and interacting with remote providers such as Google Drive or Dropbox. 


**Other Workflow Managers**
---------------------------

- `CCTools <https://cctools.readthedocs.io/en/latest/>`_ offers `Makeflow <https://cctools.readthedocs.io/en/latest/makeflow/>`_ a workflow management system similar to Snakemake and also `WorkQueue <https://cctools.readthedocs.io/en/latest/work_queue/>`_ for scaling-up through Distributed Computing for customized and efficient utilization of resources. Read more `here <http://ccl.cse.nd.edu/software/tutorials/acic19/>`_.
- `NextFlow <https://www.nextflow.io/>`_


Additional information, help
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- `Snakemake Read The Docs <https://snakemake.readthedocs.io/en/stable/#>`_

- `Snakemake Tutorial <https://snakemake.readthedocs.io/en/stable/tutorial/tutorial.html#tutorial>`_

- Search for an answer: `CyVerse Learning Center <http://learning.cyverse.org>`_ or `CyVerse Wiki <https://wiki.cyverse.org>`_

- Contact CyVerse support by clicking the intercom button on the page.

----

**Fix or improve this documentation**

- On Github: `Repo link <https://github.com/CyVerse-learning-materials/fastqc_quickstart>`_
- Send feedback: `Tutorials@CyVerse.org <Tutorials@CyVerse.org>`_

----

|Home_Icon|_
`Learning Center Home`_


.. |smake-vice| image:: https://de.cyverse.org/Powered-By-CyVerse-blue.svg
.. _smake-vice: https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=7a62a49e-7fee-4822-b128-a1b2485e2941&app-id=9e989f50-6109-11ea-ab9d-008cfa5ae621


.. |CyVerse logo| image:: ./img/cyverse_rgb.png
    :width: 500
    :height: 100
.. _CyVerse logo: http://learning.cyverse.org/
.. |Home_Icon| image:: ./img/homeicon.png
    :width: 25
    :height: 25
.. _Home_Icon: http://learning.cyverse.org/
.. |discovery_enviornment| raw:: html

    <a href="https://de.cyverse.org/de/" target="_blank">Discovery Environment</a>
