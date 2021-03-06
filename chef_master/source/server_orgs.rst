=====================================================
Organizations, Groups, and Users
=====================================================

.. warning:: This topic is a work in progress.

.. include:: ../../includes_server_rbac/includes_server_rbac.rst

|chef server oec| uses organizations, groups, and users to define role-based access control:

.. list-table::
   :widths: 60 420
   :header-rows: 1

   * - Feature
     - Description
   * - .. image:: ../../images/icon_server_organization.png
     - .. include:: ../../includes_server_rbac/includes_server_rbac_orgs.rst
   * - .. image:: ../../images/icon_server_group.png
     - .. include:: ../../includes_server_rbac/includes_server_rbac_groups.rst
   * - .. image:: ../../images/icon_server_users.png
     - .. include:: ../../includes_server_rbac/includes_server_rbac_users.rst
   * - .. image:: ../../images/icon_chef_client.png
     - .. include:: ../../includes_server_rbac/includes_server_rbac_clients.rst

A single instance of |chef server oec| can support many organizations. Each organization has a unique set of groups and users. Each organization manages a unique set of nodes, on which a |chef client| is installed and configured so that it may interact with a single organization on the |chef server|.

.. image:: ../../images/server_rbac_orgs_groups_and_users.png

A user may belong to multiple organizations under the following conditions: role-based access control is configured per-organization, for a single user to interact with the |chef server| using |knife| from the same |chef repo|, that user may need to edit their |knife rb| file prior to that interaction.

Permissions
=====================================================
.. include:: ../../includes_server_rbac/includes_server_rbac_permissions.rst

Object Permissions
-----------------------------------------------------
.. include:: ../../includes_server_rbac/includes_server_rbac_permissions_object.rst

Global Permissions
-----------------------------------------------------
.. include:: ../../includes_server_rbac/includes_server_rbac_permissions_global.rst

Default Groups
=====================================================
.. include:: ../../includes_server_rbac/includes_server_rbac_groups_default.rst

Multiple Organizations
=====================================================
The |chef server oec| supports using as many organizations as required. This can be useful when:

* Multiple product groups need to be supported, but each product group has its own security requirements, schedule, and goals
* Updates occur across the company on completely different schedules; use organizations to group nodes by schedule
* Ensures that individual teams can define their own objects and object types---data bags, environments, roles, and cookbooks---as needed
* Ensures that the entire organization is using the same toolset, approach, and system
* Sharing the same physical hardware and support team across organizations


|push jobs| Groups
=====================================================

.. include:: ../../includes_push_jobs/includes_push_jobs.rst

.. include:: ../../includes_server_rbac/includes_server_rbac_groups_push_jobs.rst

|reporting| Groups
=====================================================

.. include:: ../../includes_reporting/includes_reporting.rst

.. include:: ../../includes_server_rbac/includes_server_rbac_groups_reporting.rst
