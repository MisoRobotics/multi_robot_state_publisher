^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package robot_state_publisher
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.14.0 (2022-01-12)
-------------------
* RAD-96: Update for noetic
  Update package dependencies and add conditional to CMakeLists.txt.
* Migrate to Python 3
  Update to work with Python 3 and Noetic.
* Bump version to 2.0.0
  Bump major version for next release.
* Merge pull request `#1 <https://github.com/MisoRobotics/multi_robot_state_publisher/issues/1>`_ from rsinnet/kinetic-devel
  Create multi_robot_state_publisher
* Disable tests for now
  Disable tests after the refactor. They need to be updated, but
  everything is working and probably won't need to make any additional
  changes so not much value in the tests at this point since the tests
  established already that the algorithms are correct.
* Rename a confusing variable
  Rename last_publish_time\_ to last_update_time\_ now that responsibilities
  have been shifted around.
* Add docstrings to public members
  Add docstrings for classes and public members.
* Refactor data flow and execution model
  Create a new class to hold all robots. Change publishing to happen once
  in main loop. Publish all TFs in one message.
* Add README.md
  Add a README which describes the usage of the new node.
* Refactor data flow and execution model
  Create a new class to hold all robots. Change publishing to happen once
  in main loop. Publish all TFs in one message.
* Update tests
  Update tests for new package name and interface changes.
* Clean up main function
  Use a range-based for loop in the main function.
* Move JointStateListener to library
  Move code to a library and add an separate executable with the main
  function.
* Update to new namespace
  Move code to multi_robot_state_publisher namespace.
* Update CMakeLists.txt
  Update required CMake version. Update compiler definitions. Change
  project name.
* Update package.xml to Package Format 2
  Upgrade to newer catkin package format. Update maintainers.
* Format URDF files
  Save them with auto-formatting with no changes.
* Add .clang-format and apply
  Add formatting file for clang-format and apply to all relevant files.
* Add .cmake-format
  Add style file for CMake and run it on CMakeLists.txt.
* Add .editorconfig file
  Add a generic .editorconfig for auto formatting.
* Contributors: Ryan Sinnet

10.1.1 (2022-03-25)
-------------------
* Merge branch 'user/rsinnet/RAD-171' into develop
* RAD-171: Add labeling workflow
  Add a labeling workflow to apply the `flippy` label.
* Merge pull request `#3 <https://github.com/MisoRobotics/multi_robot_state_publisher/issues/3>`_ from MisoRobotics/master
  Backmerge master into develop for chippy-10.1.0
* Contributors: Ryan Sinnet, Zach Zweig Vinegar

10.1.0 (2022-01-12)
-------------------
* 1.14.0
* Add changelog for chippy-1.14.0
  Add changelog for chippy-1.14.0.
* RAD-96: Update for noetic
  Update package dependencies and add conditional to CMakeLists.txt.
* Migrate to Python 3
  Update to work with Python 3 and Noetic.
* Bump version to 2.0.0
  Bump major version for next release.
* Merge pull request `#1 <https://github.com/MisoRobotics/multi_robot_state_publisher/issues/1>`_ from rsinnet/kinetic-devel
  Create multi_robot_state_publisher
* Disable tests for now
  Disable tests after the refactor. They need to be updated, but
  everything is working and probably won't need to make any additional
  changes so not much value in the tests at this point since the tests
  established already that the algorithms are correct.
* Rename a confusing variable
  Rename last_publish_time\_ to last_update_time\_ now that responsibilities
  have been shifted around.
* Add docstrings to public members
  Add docstrings for classes and public members.
* Refactor data flow and execution model
  Create a new class to hold all robots. Change publishing to happen once
  in main loop. Publish all TFs in one message.
* Add README.md
  Add a README which describes the usage of the new node.
* Refactor data flow and execution model
  Create a new class to hold all robots. Change publishing to happen once
  in main loop. Publish all TFs in one message.
* Update tests
  Update tests for new package name and interface changes.
* Clean up main function
  Use a range-based for loop in the main function.
* Move JointStateListener to library
  Move code to a library and add an separate executable with the main
  function.
* Update to new namespace
  Move code to multi_robot_state_publisher namespace.
* Update CMakeLists.txt
  Update required CMake version. Update compiler definitions. Change
  project name.
* Update package.xml to Package Format 2
  Upgrade to newer catkin package format. Update maintainers.
* Format URDF files
  Save them with auto-formatting with no changes.
* Add .clang-format and apply
  Add formatting file for clang-format and apply to all relevant files.
* Add .cmake-format
  Add style file for CMake and run it on CMakeLists.txt.
* Add .editorconfig file
  Add a generic .editorconfig for auto formatting.
* Contributors: Ryan Sinnet, Zach Zweig Vinegar

1.13.7 (2019-08-27)
-------------------
* Remove treefksolver completely from the repository. (`#100 <https://github.com/ros/robot_state_publisher/issues/100>`_) (`#101 <https://github.com/ros/robot_state_publisher/issues/101>`_)
* Add Ian as a maintainer for robot_state_publisher (`#95 <https://github.com/ros/robot_state_publisher/issues/95>`_)
* Fixed problem when building static library version (`#92 <https://github.com/ros/robot_state_publisher/issues/92>`_)
* Contributors: Chris Lalancette, Shane Loretz, ivanpauno

1.13.6 (2018-04-05)
-------------------
* added warning when joint is found in joint message but not in the urdf (`#83 <https://github.com/ros/robot_state_publisher/issues/83>`_)
* added ros_warn if JointStateMessage is older than 30 seconds (`#84 <https://github.com/ros/robot_state_publisher/issues/84>`_)
* Add tcp_no_delay to joint_states subscriber (`#80 <https://github.com/ros/robot_state_publisher/issues/80>`_)
* make rostest in CMakeLists optional (`ros/rosdistro#3010 <https://github.com/ros/rosdistro/issues/3010>`_) (`#75 <https://github.com/ros/robot_state_publisher/issues/75>`_)
* Added c++11 target_compile_options (`#78 <https://github.com/ros/robot_state_publisher/issues/78>`_)
* Contributors: Lukas Bulwahn, Shane Loretz, Victor Lopez, jgueldenstein

1.13.5 (2017-04-11)
-------------------
* Style cleanup throughout the tree.
* add Chris and Shane as maintainers (`#70 <https://github.com/ros/robot_state_publisher/issues/70>`_)
* Contributors: Chris Lalancette, William Woodall

1.13.4 (2017-01-05)
-------------------
* Use ``urdf::*ShredPtr`` instead of ``boost::shared_ptr`` (`#60 <https://github.com/ros/robot_state_publisher/issues/60>`_)
* Error log for empty JointState.position was downgraded to a throttled warning (`#64 <https://github.com/ros/robot_state_publisher/issues/64>`_)
* Contributors: Jochen Sprickerhof, Sébastien BARTHÉLÉMY

1.13.3 (2016-10-20)
-------------------
* Added a new parameter "ignore_timestamp" (`#65 <https://github.com/ros/robot_state_publisher/issues/65>`_)
* Fixed joints are not published over tf_static by default (`#56 <https://github.com/ros/robot_state_publisher/issues/56>`_)
* Fixed segfault on undefined robot_description (`#61 <https://github.com/ros/robot_state_publisher/issues/61>`_)
* Fixed cmake eigen3 warning (`#62 <https://github.com/ros/robot_state_publisher/issues/62>`_)
* Contributors: Davide Faconti, Ioan A Sucan, Johannes Meyer, Robert Haschke

1.13.2 (2016-06-10)
-------------------
* Add target_link_libraries for joint_state_listener library + install it (`#54 <https://github.com/ros/robot_state_publisher//issues/54>`_)
* Contributors: Kartik Mohta

1.13.1 (2016-05-20)
-------------------
* Add back future dating for robot_state_publisher (`#49 <https://github.com/ros/robot_state_publisher/issues/49>`_) (`#51 <https://github.com/ros/robot_state_publisher/issues/51>`_)
* Fix subclassing test (`#48 <https://github.com/ros/robot_state_publisher/issues/48>`_)
* Support for subclassing (`#45 <https://github.com/ros/robot_state_publisher/issues/45>`_)
  * Add joint_state_listener as a library
* Contributors: Jackie Kay

1.13.0 (2016-04-12)
-------------------
* fix bad rebase
* Contributors: Jackie Kay, Paul Bovbel

1.12.1 (2016-02-22)
-------------------
* Merge pull request `#42 <https://github.com/ros/robot_state_publisher/issues/42>`_ from ros/fix_tests_jade
  Fix tests for Jade
* Correct failing tests
* Re-enabling rostests
* Merge pull request `#39 <https://github.com/ros/robot_state_publisher/issues/39>`_ from scpeters/issue_38
* Fix API break in publishFixedTransforms
  A bool argument was added to
  RobotStatePublisher::publishFixedTransforms
  which broke API.
  I've added a default value of false, to match
  the default specified in the JointStateListener
  constructor.
* Contributors: Jackie Kay, Jonathan Bohren, Steven Peters

1.12.0 (2015-10-21)
-------------------
* Merge pull request `#37 <https://github.com/ros/robot_state_publisher/issues/37>`_ from clearpathrobotics/static-default
  Publish fixed joints over tf_static by default
* Merge pull request `#34 <https://github.com/ros/robot_state_publisher/issues/34>`_ from ros/tf2-static-jade
  Port to tf2 and enable using static broadcaster
* Merge pull request `#32 <https://github.com/ros/robot_state_publisher/issues/32>`_ from `shadow-robot/fix_issue#19 <https://github.com/shadow-robot/fix_issue/issues/19>`_
  Check URDF to distinguish fixed joints from floating joints. Floating joint are ignored by the publisher.
* Merge pull request `#26 <https://github.com/ros/robot_state_publisher/issues/26>`_ from xqms/remove-debug
  get rid of argv[0] debug output on startup
* Contributors: David Lu!!, Ioan A Sucan, Jackie Kay, Max Schwarz, Paul Bovbel, Toni Oliver

1.11.1 (2016-02-22)
-------------------
* Merge pull request `#41 <https://github.com/ros/robot_state_publisher/issues/41>`_ from ros/fix_tests_indigo
  Re-enable and clean up rostests
* Correct failing tests
* Re-enabling rostests
* Fix API break in publishFixedTransforms
  A bool argument was added to
  RobotStatePublisher::publishFixedTransforms
  which broke API.
  I've added a default value of false, to match
  the default specified in the JointStateListener
  constructor.
* Contributors: Jackie Kay, Jonathan Bohren, Steven Peters

1.11.0 (2015-10-21)
-------------------
* Merge pull request `#28 <https://github.com/ros/robot_state_publisher/issues/28>`_ from clearpathrobotics/tf2-static

1.10.4 (2014-11-30)
-------------------
* Merge pull request `#21 <https://github.com/ros/robot_state_publisher/issues/21>`_ from rcodddow/patch-1
* Fix for joint transforms not being published anymore after a clock reset (e.g. when playing a bagfile and looping)
* Contributors: Ioan A Sucan, Robert Codd-Downey, Timm Linder

1.10.3 (2014-07-24)
-------------------
* add version depend on orocos_kdl >= 1.3.0
  Conflicts:
  package.xml
* Update KDL SegmentMap interface to optionally use shared pointers
  The KDL Tree API optionally uses shared pointers on platforms where
  the STL containers don't support incomplete types.
* Contributors: Brian Jensen, William Woodall

1.10.0 (2014-03-03)
-------------------
* minor style fixes
* Add support for mimic tag.
* Contributors: Ioan Sucan, Konrad Banachowicz
