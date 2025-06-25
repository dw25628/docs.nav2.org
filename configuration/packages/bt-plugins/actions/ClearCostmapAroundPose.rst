.. _bt_clear_entire_costmap_around_pose_action:


ClearCostmapAroundPose
=======================

Action to call a costmap clearing around a passed pose.

Input Ports
-----------

:reset_distance:

  ============== =======
  Type           Default
  -------------- -------
  double         1
  ============== =======

  Description
    	side size of the square area centered on the pose that will be cleared on the costmap (the rest of the costmap won't)

:pose:

  ================================ =========
  Type                             Default  
  -------------------------------- ---------
  geometry_msgs::msg::PoseStamped  N/A      
  ================================ =========

  Description
    	pose around which the costmap will be cleared.

:service_name:

  ============== =======
  Type           Default
  -------------- -------
  string         N/A
  ============== =======

  Description
    	costmap service name responsible for clearing the costmap.

:server_timeout:

  ============== =======
  Type           Default
  -------------- -------
  double         10
  ============== =======

  Description
    	Action server timeout (ms).

Example
-------

.. code-block:: xml

  <ClearCostmapAroundPose name="ClearCostmapAroundPose-Subtree" service_name="global_costmap/clear_around_pose_global_costmap" pose="{goal}" reset_distance="5.0"/>
