cmake_minimum_required(VERSION 2.8.3)
project(nw_mico)

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(FILES
   mico-modified.urdf
   #DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/urdf
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
 )
install(DIRECTORY meshes
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
   FILES_MATCHING PATTERN "*.dae"
 )
