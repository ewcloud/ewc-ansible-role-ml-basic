EWC Ansible Role ML Basic
=========================

Create a conda environment with the basic Machine Learning packages such as torch, xgboost, and scikit-learn. Check the `templat

Requirements
------------
This ansible role depends on ewc-ansible-role-conda

Role Variables
--------------
 - `ml_basic_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
 - `ml_basic_env_name`: Name of the environment containing the software stack. Default: ml-basic
 - `ml_basic_env_path`: Path to the environment containing the software stack. Default: `{{ conda_prefix }}/envs/{{ ml_basic_env_name }}`
 - `ml_basic_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
 - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
 - `conda_user`: User owning the conda installation. Default: `root`

Example Playbook
----------------

    - hosts: all
      roles:
         -  ewc-ansible-role-ml-basic

License
-------

Apache 2.0.

Author Information
------------------

ECMWF for the European Weather Cloud