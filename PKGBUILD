# Script generated with Bloom
pkgdesc="ROS - Provides nonlinear state estimation through sensor fusion of an abritrary number of sensors."
url='http://ros.org/wiki/robot_localization'

pkgname='ros-kinetic-robot-localization'
pkgver='2.4.3_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('eigen3'
'python2-catkin_pkg'
'ros-kinetic-catkin'
'ros-kinetic-cmake-modules'
'ros-kinetic-diagnostic-msgs'
'ros-kinetic-diagnostic-updater'
'ros-kinetic-eigen-conversions'
'ros-kinetic-geographic-msgs'
'ros-kinetic-geometry-msgs'
'ros-kinetic-message-filters'
'ros-kinetic-message-generation'
'ros-kinetic-nav-msgs'
'ros-kinetic-rosbag'
'ros-kinetic-roscpp'
'ros-kinetic-roslint'
'ros-kinetic-rostest'
'ros-kinetic-rosunit'
'ros-kinetic-sensor-msgs'
'ros-kinetic-std-msgs'
'ros-kinetic-std-srvs'
'ros-kinetic-tf2'
'ros-kinetic-tf2-geometry-msgs'
'ros-kinetic-tf2-ros'
'ros-kinetic-xmlrpcpp'
'yaml-cpp'
)

depends=('eigen3'
'ros-kinetic-cmake-modules'
'ros-kinetic-diagnostic-msgs'
'ros-kinetic-diagnostic-updater'
'ros-kinetic-eigen-conversions'
'ros-kinetic-geographic-msgs'
'ros-kinetic-geometry-msgs'
'ros-kinetic-message-filters'
'ros-kinetic-message-runtime'
'ros-kinetic-nav-msgs'
'ros-kinetic-roscpp'
'ros-kinetic-sensor-msgs'
'ros-kinetic-std-msgs'
'ros-kinetic-std-srvs'
'ros-kinetic-tf2'
'ros-kinetic-tf2-geometry-msgs'
'ros-kinetic-tf2-ros'
'ros-kinetic-xmlrpcpp'
'yaml-cpp'
)

conflicts=()
replaces=()

_dir=robot_localization
source=()
md5sums=()

prepare() {
    cp -R $startdir/robot_localization $srcdir/robot_localization
}

build() {
  # Use ROS environment variables
  source /usr/share/ros-build-tools/clear-ros-env.sh
  [ -f /opt/ros/kinetic/setup.bash ] && source /opt/ros/kinetic/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/kinetic \
        -DPYTHON_EXECUTABLE=/usr/bin/python2 \
        -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
        -DPYTHON_LIBRARY=/usr/lib/libpython2.7.so \
        -DPYTHON_BASENAME=-python2.7 \
        -DSETUPTOOLS_DEB_LAYOUT=OFF
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}

