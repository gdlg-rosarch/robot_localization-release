# Script generated with Bloom
pkgdesc="ROS - Provides nonlinear state estimation through sensor fusion of an abritrary number of sensors."
url='http://ros.org/wiki/robot_localization'

pkgname='ros-lunar-robot-localization'
pkgver='2.5.2_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('eigen3'
'python2-catkin_pkg'
'ros-lunar-catkin'
'ros-lunar-cmake-modules'
'ros-lunar-diagnostic-msgs'
'ros-lunar-diagnostic-updater'
'ros-lunar-eigen-conversions'
'ros-lunar-geographic-msgs'
'ros-lunar-geometry-msgs'
'ros-lunar-message-filters'
'ros-lunar-message-generation'
'ros-lunar-nav-msgs'
'ros-lunar-nodelet'
'ros-lunar-rosbag'
'ros-lunar-roscpp'
'ros-lunar-roslint'
'ros-lunar-rostest'
'ros-lunar-rosunit'
'ros-lunar-sensor-msgs'
'ros-lunar-std-msgs'
'ros-lunar-std-srvs'
'ros-lunar-tf2'
'ros-lunar-tf2-geometry-msgs'
'ros-lunar-tf2-ros'
'ros-lunar-xmlrpcpp'
'yaml-cpp'
)

depends=('eigen3'
'ros-lunar-cmake-modules'
'ros-lunar-diagnostic-msgs'
'ros-lunar-diagnostic-updater'
'ros-lunar-eigen-conversions'
'ros-lunar-geographic-msgs'
'ros-lunar-geometry-msgs'
'ros-lunar-message-filters'
'ros-lunar-message-runtime'
'ros-lunar-nav-msgs'
'ros-lunar-nodelet'
'ros-lunar-roscpp'
'ros-lunar-sensor-msgs'
'ros-lunar-std-msgs'
'ros-lunar-std-srvs'
'ros-lunar-tf2'
'ros-lunar-tf2-geometry-msgs'
'ros-lunar-tf2-ros'
'ros-lunar-xmlrpcpp'
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
  [ -f /opt/ros/lunar/setup.bash ] && source /opt/ros/lunar/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/lunar \
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

