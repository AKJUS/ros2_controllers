cmake_minimum_required(VERSION 3.16)
project(range_sensor_broadcaster)

find_package(ros2_control_cmake REQUIRED)
set_compiler_options()
export_windows_symbols()

set(THIS_PACKAGE_INCLUDE_DEPENDS
  controller_interface
  generate_parameter_library
  hardware_interface
  pluginlib
  rclcpp
  rclcpp_lifecycle
  realtime_tools
  sensor_msgs
)

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(backward_ros REQUIRED)
foreach(Dependency IN ITEMS ${THIS_PACKAGE_INCLUDE_DEPENDS})
  find_package(${Dependency} REQUIRED)
endforeach()


generate_parameter_library(range_sensor_broadcaster_parameters
  src/range_sensor_broadcaster_parameters.yaml
)

add_library(
  range_sensor_broadcaster SHARED
  src/range_sensor_broadcaster.cpp
)
target_include_directories(range_sensor_broadcaster
  PRIVATE $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
  PRIVATE $<INSTALL_INTERFACE:include>
)
target_link_libraries(range_sensor_broadcaster PUBLIC
                      range_sensor_broadcaster_parameters
                      controller_interface::controller_interface
                      hardware_interface::hardware_interface
                      pluginlib::pluginlib
                      rclcpp::rclcpp
                      rclcpp_lifecycle::rclcpp_lifecycle
                      realtime_tools::realtime_tools
                      ${sensor_msgs_TARGETS})

pluginlib_export_plugin_description_file(
  controller_interface range_sensor_broadcaster.xml)

if(BUILD_TESTING)
  find_package(ament_cmake_gmock REQUIRED)
  find_package(controller_manager REQUIRED)
  find_package(hardware_interface REQUIRED)
  find_package(ros2_control_test_assets REQUIRED)

  add_definitions(-DTEST_FILES_DIRECTORY="${CMAKE_CURRENT_SOURCE_DIR}/test")
  ament_add_gmock(test_load_range_sensor_broadcaster test/test_load_range_sensor_broadcaster.cpp)
  target_include_directories(test_load_range_sensor_broadcaster PRIVATE include)
  target_link_libraries(test_load_range_sensor_broadcaster
    range_sensor_broadcaster
    controller_manager::controller_manager
    hardware_interface::hardware_interface
    ros2_control_test_assets::ros2_control_test_assets
  )

  add_rostest_with_parameters_gmock(test_range_sensor_broadcaster
    test/test_range_sensor_broadcaster.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/test/range_sensor_broadcaster_params.yaml)
  target_include_directories(test_range_sensor_broadcaster PRIVATE include)
  target_link_libraries(test_range_sensor_broadcaster
    range_sensor_broadcaster
  )
endif()

install(
  DIRECTORY include/
  DESTINATION include
)

install(
  TARGETS
    range_sensor_broadcaster
    range_sensor_broadcaster_parameters
  EXPORT export_range_sensor_broadcaster
  RUNTIME DESTINATION bin
  ARCHIVE DESTINATION lib
  LIBRARY DESTINATION lib
  INCLUDES DESTINATION include
)

ament_export_targets(export_range_sensor_broadcaster HAS_LIBRARY_TARGET)
ament_export_dependencies(${THIS_PACKAGE_INCLUDE_DEPENDS})

ament_package()
