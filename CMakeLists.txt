set(source_files
  model/lifi-propagation-loss-model.cc
  model/lifi-snr.cc
  model/lifi-phy.cc
  model/lifi-mobility-model.cc 
  model/lifi-error-model.cc
  model/lifi-channel.cc
  model/lifi-net-device.cc
  model/lifi-tx-net-device.cc
  model/lifi-rx-net-device.cc
  model/lifi-mac-low.cc
  model/lifi-ap-mac.cc
  model/lifi-sta-mac.cc
  model/lifi-tx-mac.cc
  model/lifi-rx-mac.cc
  model/lifi-mac-queue.cc
  model/lifi-user-device-infos.cc
  model/beacon-response-tag.cc
  model/lifi-application.cc
  model/lifi-regular-mac.cc
  model/measurement-report.cc
  model/lifi-capability-information.cc
  model/mac-resources-tag.cc
  model/remote-station-manager.cc
  helper/lifi-helper.cc 
  helper/lifi-phy-helper.cc
  helper/lifi-mac-helper.cc
  model/lifi-random-waypoint-mobility-model.cc
  model/lifi-constant-velocity-mobility-model.cc
  model/received-data-model.cc
  model/my-tag.cc
)

set(header_files
  model/lifi-phy.h
  model/lifi-snr.h
  model/lifi-propagation-loss-model.h
  model/lifi-mobility-model.h 
  model/lifi-error-model.h
  model/lifi-channel.h
  model/lifi-ap-mac.h
  model/lifi-sta-mac.h
  model/lifi-tx-mac.h
  model/lifi-rx-mac.h
  model/lifi-net-device.h
  model/lifi-tx-net-device.h
  model/lifi-rx-net-device.h
  model/lifi-mac-low.h
  model/lifi-mac-queue.h
  model/lifi-user-device-infos.h
  model/lifi-regular-mac.h
  model/lifi-application.h 
  model/measurement-report.h
  model/lifi-capability-information.h
  model/mac-resources-tag.h
  model/beacon-response-tag.h
  helper/lifi-helper.h 
  helper/lifi-phy-helper.h
  helper/lifi-mac-helper.h
  model/remote-station-manager.h
  model/commons.h
  model/lifi-random-waypoint-mobility-model.h
  model/lifi-constant-velocity-mobility-model.h
  model/received-data-model.h
  model/my-tag.h
)


# set(test_sources
#     test/vlc-test-suite.cc
# )

build_lib(
  LIBNAME lifi
  SOURCE_FILES ${source_files}
  HEADER_FILES ${header_files}
  LIBRARIES_TO_LINK
    ${libinternet}
    ${libmobility}
  # TEST_SOURCES ${test_sources}
)
