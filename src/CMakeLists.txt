find_package(glog)
find_package(ky_timer)

add_library(ky_observability
        observer.cc
        observable.cc)
target_link_libraries(ky_observability
        PUBLIC ky_timer::ky_timer
        PRIVATE glog::glog)
KyDepsPackageLibraryTarget(ky_observability "ky/observability")
