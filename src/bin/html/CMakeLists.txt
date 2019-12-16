set(OPJ_HTML_SRC html.c)
set(OPJ_HTML_HEADER html.h)
include_directories(
  ${OPENJPEG_BINARY_DIR}/src/lib/openjp2 # opj_config.h
  ${OPENJPEG_BINARY_DIR}/src/bin/common # opj_apps_config.h
  ${OPENJPEG_SOURCE_DIR}/src/lib/openjp2
  ${OPENJPEG_SOURCE_DIR}/src/bin/common
  ${LCMS_INCLUDE_DIRNAME}
  ${Z_INCLUDE_DIRNAME}
  ${PNG_INCLUDE_DIRNAME}
  ${TIFF_INCLUDE_DIRNAME}
  )

add_executable(openjp2 html.c html.h)
target_link_libraries(openjp2 PUBLIC openjp2_static)
