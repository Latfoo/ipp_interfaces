# ipp_interfaces

Custom ROS2 message and service types used by the `ipp` package.

`PolygonsStamped.msg` holds a header and a list of polygons (`geometry_msgs/Polygon[]`). Used by `obstacle_publisher.py` to publish the scenario obstacles and by `mapper.py` to build the occupancy grid.

`SetPath.srv` takes a `nav_msgs/Path` and returns whether it was accepted (`bool success`). Used by `path_planner.py` to hand a new path to `path_follower.py`.
