cmake_minimum_required(VERSION 3.5)
project(spatz_interfaces)

if (NOT CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 17)
endif ()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
        "msg/ControlSetpoint.msg"
        )

ament_package()
