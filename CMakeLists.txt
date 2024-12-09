cmake_minimum_required(VERSION 3.8)

project(simpleamqpclient_vendor)

# find dependencies

find_package(ament_cmake REQUIRED)
find_package(ament_cmake_vendor_package REQUIRED)

ament_vendor(simpleamqpclient_vendor
  SATISFIED ${simpleamqpclient_FOUND}
  VCS_URL https://github.com/alanxz/SimpleAmqpClient.git
  GLOBAL_HOOK
)
ament_package(
  CONFIG_EXTRAS "simpleamqpclient_vendor-extras.cmake.in"
)
