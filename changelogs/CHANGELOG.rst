========================================
Community MySQL Collection Release Notes
========================================

.. contents:: Topics


v1.0.0
======

Release Summary
---------------

This is the first proper release of the ``community.mysql`` collection.
This changelog contains all changes to the modules in this collection that were added after the release of Ansible 2.9.0.


Minor Changes
-------------

- mysql_db - add ``master_data`` parameter (https://github.com/ansible/ansible/pull/66048).
- mysql_db - add ``skip_lock_tables`` option (https://github.com/ansible/ansible/pull/66688).
- mysql_db - add the ``check_implicit_admin`` parameter (https://github.com/ansible/ansible/issues/24418).
- mysql_db - add the ``dump_extra_args`` parameter (https://github.com/ansible/ansible/pull/67747).
- mysql_db - add the ``executed_commands`` returned value (https://github.com/ansible/ansible/pull/65498).
- mysql_db - add the ``force`` parameter (https://github.com/ansible/ansible/pull/65547).
- mysql_db - add the ``restrict_config_file`` parameter (https://github.com/ansible/ansible/issues/34488).
- mysql_db - add the ``unsafe_login_password`` parameter (https://github.com/ansible/ansible/issues/63955).
- mysql_db - add the ``use_shell`` parameter (https://github.com/ansible/ansible/issues/20196).
- mysql_info - add ``exclude_fields`` parameter (https://github.com/ansible/ansible/issues/63319).
- mysql_info - add ``global_status`` filter parameter option and return (https://github.com/ansible/ansible/pull/63189).
- mysql_info - add ``return_empty_dbs`` parameter to list empty databases (https://github.com/ansible/ansible/issues/65727).
- mysql_replication - add ``channel`` parameter (https://github.com/ansible/ansible/issues/29311).
- mysql_replication - add ``connection_name`` parameter (https://github.com/ansible/ansible/issues/46243).
- mysql_replication - add ``fail_on_error`` parameter (https://github.com/ansible/ansible/pull/66252).
- mysql_replication - add ``master_delay`` parameter (https://github.com/ansible/ansible/issues/51326).
- mysql_replication - add ``master_use_gtid`` parameter (https://github.com/ansible/ansible/pull/62648).
- mysql_replication - add ``queries`` return value (https://github.com/ansible/ansible/pull/63036).
- mysql_replication - add support of ``resetmaster`` choice to ``mode`` parameter (https://github.com/ansible/ansible/issues/42870).
- mysql_user - ``priv`` parameter can be string or dictionary (https://github.com/ansible/ansible/issues/57533).
- mysql_user - add TLS REQUIRES parameters (https://github.com/ansible-collections/community.mysql/pull/9).
- mysql_user - add ``plugin_auth_string`` parameter (https://github.com/ansible/ansible/pull/44267).
- mysql_user - add ``plugin_hash_string`` parameter (https://github.com/ansible/ansible/pull/44267).
- mysql_user - add ``plugin`` parameter (https://github.com/ansible/ansible/pull/44267).
- mysql_user - add the resource_limits parameter (https://github.com/ansible-collections/community.general/issues/133).
- mysql_variables - add ``mode`` parameter (https://github.com/ansible/ansible/issues/60119).

Bugfixes
--------

- mysql - dont mask ``mysql_connect`` function errors from modules (https://github.com/ansible/ansible/issues/64560).
- mysql_db - fix Broken pipe error appearance when state is import and the target file is compressed (https://github.com/ansible/ansible/issues/20196).
- mysql_db - fix bug in the ``db_import`` function introduced by https://github.com/ansible/ansible/pull/56721 (https://github.com/ansible/ansible/issues/65351).
- mysql_info - add parameter for __collect to get only what are wanted (https://github.com/ansible-collections/community.general/pull/136).
- mysql_replication - allow to pass empty values to parameters (https://github.com/ansible/ansible/issues/23976).
- mysql_user - Fix idempotence when long grant lists are used (https://github.com/ansible/ansible/issues/68044)
- mysql_user - Remove false positive ``no_log`` warning for ``update_password`` option
- mysql_user - add ``INVOKE LAMBDA`` privilege support (https://github.com/ansible-collections/community.general/issues/283).
- mysql_user - add missed privileges to support (https://github.com/ansible-collections/community.general/issues/617).
- mysql_user - fix ``host_all`` arguments conversion string formatting error (https://github.com/ansible/ansible/issues/29644).
- mysql_user - fix overriding password to the same (https://github.com/ansible-collections/community.general/issues/543).
- mysql_user - fix support privileges with underscore (https://github.com/ansible/ansible/issues/66974).
- mysql_user - fix the error No database selected (https://github.com/ansible/ansible/issues/68070).
- mysql_user - make sure current_pass_hash is a string before using it in comparison (https://github.com/ansible/ansible/issues/60567).
- mysql_variable - fix the module doesn't support variables name with dot (https://github.com/ansible/ansible/issues/54239).
