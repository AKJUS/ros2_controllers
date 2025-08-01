^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package admittance_controller
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

5.5.0 (2025-07-31)
------------------
* Fix `child_frame_id` in controller_state_msg (`#1601 <https://github.com/ros-controls/ros2_controllers/issues/1601>`_)
* Contributors: Rehan Shah

5.4.0 (2025-07-23)
------------------
* Use new handles API in ros2_controllers to fix deprecation warnings (`#1566 <https://github.com/ros-controls/ros2_controllers/issues/1566>`_)
* Contributors: Sanjeev Kumar

5.3.0 (2025-07-14)
------------------
* Use ParamListener::try_get_params to Avoid Blocking in Real-Time Contexts (`#1198 <https://github.com/ros-controls/ros2_controllers/issues/1198>`_)
* Update realtime containers (`#1721 <https://github.com/ros-controls/ros2_controllers/issues/1721>`_)
* Contributors: Christoph Fröhlich, Kenta Kato

5.2.0 (2025-06-23)
------------------

5.1.0 (2025-06-11)
------------------

5.0.2 (2025-05-26)
------------------

5.0.1 (2025-05-24)
------------------
* Use target_link_libraries instead of ament_target_dependencies (`#1697 <https://github.com/ros-controls/ros2_controllers/issues/1697>`_)
* Contributors: Sai Kishor Kothakota

5.0.0 (2025-05-17)
------------------
* [AdmittanceController] Remove superfluous `admittance_tranforms\_` structure (`#1668 <https://github.com/ros-controls/ros2_controllers/issues/1668>`_)
* Contributors: Geethik Mylapur

4.24.0 (2025-04-27)
-------------------

4.23.0 (2025-04-10)
-------------------
* Bump version of pre-commit hooks (`#1618 <https://github.com/ros-controls/ros2_controllers/issues/1618>`_)
* Use global cmake macros and fix gcc-10 build (`#1527 <https://github.com/ros-controls/ros2_controllers/issues/1527>`_)
* Replace RCLCPP\_*_STREAM macros with RCLCPP\_* (`#1600 <https://github.com/ros-controls/ros2_controllers/issues/1600>`_)
* Contributors: Christoph Fröhlich, Vedant Randive, github-actions[bot]

4.22.0 (2025-03-17)
-------------------

4.21.0 (2025-03-01)
-------------------
* Cleanup dependencies (add `angles`, rm `filters`) (`#1555 <https://github.com/ros-controls/ros2_controllers/issues/1555>`_)
* [Admittance] multiple state/command interfaces (`#1196 <https://github.com/ros-controls/ros2_controllers/issues/1196>`_)
* Fix the exported interface naming in the chainable controllers (`#1528 <https://github.com/ros-controls/ros2_controllers/issues/1528>`_)
* Remove dependency of admittance controller on JTC (`#1532 <https://github.com/ros-controls/ros2_controllers/issues/1532>`_)
* Contributors: Christoph Fröhlich, Marco Magri, Sai Kishor Kothakota

4.20.0 (2025-01-29)
-------------------
* Remove empty callbacks (`#1488 <https://github.com/ros-controls/ros2_controllers/issues/1488>`_)
* Update paths of GPL includes (`#1487 <https://github.com/ros-controls/ros2_controllers/issues/1487>`_)
* Contributors: Christoph Fröhlich, Julia Jia

4.19.0 (2025-01-13)
-------------------
* Remove visibility macros (`#1451 <https://github.com/ros-controls/ros2_controllers/issues/1451>`_)
* Contributors: Bence Magyar

4.18.0 (2024-12-19)
-------------------
* [CI] Add clang job and setup concurrency (`#1407 <https://github.com/ros-controls/ros2_controllers/issues/1407>`_)
* Add wrench offset for admittance controller (`#1249 <https://github.com/ros-controls/ros2_controllers/issues/1249>`_)
* Contributors: Christoph Fröhlich, Lennart Nachtigall

4.17.0 (2024-12-07)
-------------------
* Use the .hpp headers from `realtime_tools` package (`#1406 <https://github.com/ros-controls/ros2_controllers/issues/1406>`_)
* Add few warning flags to error in all ros2_controllers packages and fix tests (`#1370 <https://github.com/ros-controls/ros2_controllers/issues/1370>`_)
* Update maintainers and add url tags (`#1363 <https://github.com/ros-controls/ros2_controllers/issues/1363>`_)
* Contributors: Christoph Fröhlich, Sai Kishor Kothakota

4.16.0 (2024-11-08)
-------------------
* Adding use of robot description parameter in the Admittance Controller (`#1247 <https://github.com/ros-controls/ros2_controllers/issues/1247>`_)
* Contributors: Dr. Denis, Kevin DeMarco, Nikola Banovic, Bence Magyar, Christoph Fröhlich

4.15.0 (2024-10-07)
-------------------

4.14.0 (2024-09-11)
-------------------

4.13.0 (2024-08-22)
-------------------
* Fix segfault at reconfigure of AdmittanceController (`#1248 <https://github.com/ros-controls/ros2_controllers/issues/1248>`_)
* Fixes tests to work with use_global_arguments NodeOptions parameter  (`#1256 <https://github.com/ros-controls/ros2_controllers/issues/1256>`_)
* Contributors: Lennart Nachtigall, Sai Kishor Kothakota

4.12.1 (2024-08-14)
-------------------
* Fix admittance controller interface read/write logic (`#1232 <https://github.com/ros-controls/ros2_controllers/issues/1232>`_)
* Contributors: Nikola Banović

4.12.0 (2024-07-23)
-------------------
* Change the subscription timeout in the tests to 5ms (`#1219 <https://github.com/ros-controls/ros2_controllers/issues/1219>`_)
* Unused header cleanup (`#1199 <https://github.com/ros-controls/ros2_controllers/issues/1199>`_)
* Fix WaitSet issue in tests  (`#1206 <https://github.com/ros-controls/ros2_controllers/issues/1206>`_)
* Fix parallel gripper controller CI (`#1202 <https://github.com/ros-controls/ros2_controllers/issues/1202>`_)
* Contributors: Henry Moore, Sai Kishor Kothakota

4.11.0 (2024-07-09)
-------------------
* added changes corresponding to the logger and clock propagation in ResourceManager (`#1184 <https://github.com/ros-controls/ros2_controllers/issues/1184>`_)
* Contributors: Sai Kishor Kothakota

4.10.0 (2024-07-01)
-------------------

4.9.0 (2024-06-05)
------------------

4.8.0 (2024-05-14)
------------------

4.7.0 (2024-03-22)
------------------
* Use CMake target for eigen (`#1058 <https://github.com/ros-controls/ros2_controllers/issues/1058>`_)
* Contributors: Christoph Fröhlich

4.6.0 (2024-02-12)
------------------
* Add test_depend on `hardware_interface_testing` (`#1018 <https://github.com/ros-controls/ros2_controllers/issues/1018>`_)
* Contributors: Christoph Fröhlich

4.5.0 (2024-01-31)
------------------
* Add tests for `interface_configuration_type` consistently (`#899 <https://github.com/ros-controls/ros2_controllers/issues/899>`_)
* Let sphinx add parameter description with nested structures to documentation (`#652 <https://github.com/ros-controls/ros2_controllers/issues/652>`_)
* Contributors: Christoph Fröhlich

4.4.0 (2024-01-11)
------------------

4.3.0 (2024-01-08)
------------------
* Remove robot description param from admittance YAML (`#963 <https://github.com/ros-controls/ros2_controllers/issues/963>`_)
* Add few warning flags to error (`#961 <https://github.com/ros-controls/ros2_controllers/issues/961>`_)
* Contributors: Abishalini Sivaraman, Sai Kishor Kothakota

4.2.0 (2023-12-12)
------------------

4.1.0 (2023-12-01)
------------------

4.0.0 (2023-11-21)
------------------
* fix tests for API break of passing controller manager update rate in init method (`#854 <https://github.com/ros-controls/ros2_controllers/issues/854>`_)
* Adjust tests after passing URDF to controllers (`#817 <https://github.com/ros-controls/ros2_controllers/issues/817>`_)
* Contributors: Bence Magyar, Sai Kishor Kothakota

3.17.0 (2023-10-31)
-------------------

3.16.0 (2023-09-20)
-------------------

3.15.0 (2023-09-11)
-------------------
* Update docs for diff drive controller (`#751 <https://github.com/ros-controls/ros2_controllers/issues/751>`_)
* Contributors: Christoph Fröhlich

3.14.0 (2023-08-16)
-------------------

3.13.0 (2023-08-04)
-------------------
* Fix out of bound access in admittance controller (`#721 <https://github.com/ros-controls/ros2_controllers/issues/721>`_)
* Contributors: Abishalini Sivaraman

3.12.0 (2023-07-18)
-------------------
* Activate AdmittanceControllerTestParameterizedInvalidParameters (`#711 <https://github.com/ros-controls/ros2_controllers/issues/711>`_)
* Contributors: Christoph Fröhlich

3.11.0 (2023-06-24)
-------------------
* Fix cpplint (`#681 <https://github.com/ros-controls/ros2_controllers/issues/681>`_)
* Added -Wconversion flag and fix warnings (`#667 <https://github.com/ros-controls/ros2_controllers/issues/667>`_)
* Contributors: Christoph Fröhlich, gwalck

3.10.1 (2023-06-06)
-------------------

3.10.0 (2023-06-04)
-------------------
* enable ReflowComments to also use ColumnLimit on comments (`#625 <https://github.com/ros-controls/ros2_controllers/issues/625>`_)
* Contributors: Sai Kishor Kothakota

3.9.0 (2023-05-28)
------------------
* Use branch name substitution for all links (`#618 <https://github.com/ros-controls/ros2_controllers/issues/618>`_)
* Fix github links on control.ros.org (`#604 <https://github.com/ros-controls/ros2_controllers/issues/604>`_)
* Contributors: Christoph Fröhlich

3.8.0 (2023-05-14)
------------------

3.7.0 (2023-05-02)
------------------

3.6.0 (2023-04-29)
------------------
* Renovate load controller tests (`#569 <https://github.com/ros-controls/ros2_controllers/issues/569>`_)
* Fix docs format (`#589 <https://github.com/ros-controls/ros2_controllers/issues/589>`_)
* Contributors: Bence Magyar, Christoph Fröhlich

3.5.0 (2023-04-14)
------------------
* Misplaced param init in admittance_controller (`#547 <https://github.com/ros-controls/ros2_controllers/issues/547>`_)
* [Parameters] Use `gt_eq` instead of deprecated `lower_bounds` in validators (`#561 <https://github.com/ros-controls/ros2_controllers/issues/561>`_)
* Contributors: Dr. Denis, GuiHome

3.4.0 (2023-04-02)
------------------
* [AdmittanceController] Addintional argument in methods of ControllerInterface (`#553 <https://github.com/ros-controls/ros2_controllers/issues/553>`_)
* Removed auto param decl (`#546 <https://github.com/ros-controls/ros2_controllers/issues/546>`_)
* Contributors: Dr. Denis, GuiHome

3.3.0 (2023-03-07)
------------------
* Add comments about auto-generated header files (`#539 <https://github.com/ros-controls/ros2_controllers/issues/539>`_)
* Contributors: AndyZe

3.2.0 (2023-02-10)
------------------
* Fix overriding of install (`#510 <https://github.com/ros-controls/ros2_controllers/issues/510>`_)
* Contributors: Tyler Weaver, Chris Thrasher

3.1.0 (2023-01-26)
------------------

3.0.0 (2023-01-19)
------------------
* Add backward_ros to all controllers (`#489 <https://github.com/ros-controls/ros2_controllers/issues/489>`_)
* Contributors: Bence Magyar

2.15.0 (2022-12-06)
-------------------

2.14.0 (2022-11-18)
-------------------
* Bring admittance_controller version up to speed
* [AdmittanceController] Add missing dependecies for the tests (`#465 <https://github.com/ros-controls/ros2_controllers/issues/465>`_)
  We need a concrete implementation of `kinematics_interface` for tests to work. We use `kinematics_interface_kdl` implementation in the tests.
* Fix parameter library export (`#448 <https://github.com/ros-controls/ros2_controllers/issues/448>`_)
* Add generic admittance controller for TCP wrenches (`#370 <https://github.com/ros-controls/ros2_controllers/issues/370>`_)
  Co-authored-by: AndyZe <zelenak@picknik.ai>
  Co-authored-by: Denis Štogl <denis@stoglrobotics.de>
* Contributors: Bence Magyar, Denis Štogl, Paul Gesel, Tyler Weaver

* Bring admittance_controller version up to speed
* [AdmittanceController] Add missing dependecies for the tests (`#465 <https://github.com/ros-controls/ros2_controllers/issues/465>`_)
  We need a concrete implementation of `kinematics_interface` for tests to work. We use `kinematics_interface_kdl` implementation in the tests.
* Fix parameter library export (`#448 <https://github.com/ros-controls/ros2_controllers/issues/448>`_)
* Add generic admittance controller for TCP wrenches (`#370 <https://github.com/ros-controls/ros2_controllers/issues/370>`_)
  Co-authored-by: AndyZe <zelenak@picknik.ai>
  Co-authored-by: Denis Štogl <denis@stoglrobotics.de>
* Contributors: Bence Magyar, Denis Štogl, Paul Gesel, Tyler Weaver

2.13.0 (2022-10-05)
-------------------

2.12.0 (2022-09-01)
-------------------

2.11.0 (2022-08-04)
-------------------

2.10.0 (2022-08-01)
-------------------

2.9.0 (2022-07-14)
------------------

2.8.0 (2022-07-09)
------------------

2.7.0 (2022-07-03)
------------------

2.6.0 (2022-06-18)
------------------

2.5.0 (2022-05-13)
------------------

2.4.0 (2022-04-29)
------------------

2.3.0 (2022-04-21)
------------------

2.2.0 (2022-03-25)
------------------

2.1.0 (2022-02-23)
------------------

2.0.1 (2022-02-01)
------------------

2.0.0 (2022-01-28)
------------------

1.3.0 (2022-01-11)
------------------

1.2.0 (2021-12-29)
------------------

1.1.0 (2021-10-25)
------------------

1.0.0 (2021-09-29)
------------------

0.5.0 (2021-08-30)
------------------

0.4.1 (2021-07-08)
------------------

0.4.0 (2021-06-28)
------------------

0.3.1 (2021-05-23)
------------------

0.3.0 (2021-05-21)
------------------

0.2.1 (2021-05-03)
------------------

0.2.0 (2021-02-06)
------------------

0.1.2 (2021-01-07)
------------------

0.1.1 (2021-01-06)
------------------

0.1.0 (2020-12-23)
------------------
