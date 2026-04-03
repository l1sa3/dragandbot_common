cmake_minimum_required(VERSION 3.8)
project(dnb_msgs)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/Argument.msg"
  "msg/ComponentStatus.msg"
  "msg/KeTopStatus.msg"
  "msg/Program.msg"
  "msg/StringMultiArray.msg"
  "msg/ToastMessage.msg"
  "msg/ToastTranslation.msg"
  "srv/GetProgramsList.srv"
  "srv/RunProgramWithArguments.srv"
  "srv/SetInt32.srv"
  "srv/SetString.srv"
  DEPENDENCIES std_msgs 
)

ament_export_dependencies(rosidl_default_runtime)

ament_package()