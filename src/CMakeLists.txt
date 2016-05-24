# Add executable targets
########################
ADD_EXECUTABLE(led_controller_appd led_controller.c)

# Add library targets
#####################
FIND_LIBRARY(LIB_AWA libawa.so PATHS ${STAGING_DIR}/usr/lib)
TARGET_LINK_LIBRARIES(led_controller_appd ${LIB_AWA})

# Add install targets
######################
INSTALL(TARGETS led_controller_appd RUNTIME DESTINATION bin)
