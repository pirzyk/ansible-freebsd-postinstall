.. _ug_debug:

Debug
=====

To display some facts (12-18) and values of the control variables
(36-80), select the task *fp_debug* and enable the debug output. By
default, all control variables are disabled. Below is an example
configuration of a typical VM for testing

.. include:: debug-example.rst

.. note:: If you use the configuration from the Quick start guide enable *ok* hosts either by the
          environment variable ``ANSIBLE_DISPLAY_OK_HOSTS=True`` or in the configuration file
          ``display_ok_hosts=true``.

Some tasks will display additional information when the variable
:index:`fp_*_debug` is enabled.  For example, see the configuration of
sshd below. Inspect the files in the ``tasks`` directory whether
*debug* is available or not

.. include:: debug-sshd-example.rst

.. note::

   * The debug output of this role is optimized for the *yaml* callback plugin. Set the
     plugin in the environment ::

       shell> export ANSIBLE_STDOUT_CALLBACK=yaml

     or in the configuration file ::

       stdout_callback = yaml

   * See the details about the yaml callback plugin ::

       shell> ansible-doc -t callback community.general.yaml

   * See the list of other callback plugins ::

       shell> ansible-doc -t callback -l


.. seealso::

   * `Playbook Debugger <https://docs.ansible.com/ansible/latest/user_guide/playbooks_debugger.html>`_
   * `Debugging modules <https://docs.ansible.com/ansible/latest/dev_guide/debugging.html#debugging-modules>`_
   * `Python Debugging With Pdb <https://docs.python.org/3/library/pdb.html>`_
