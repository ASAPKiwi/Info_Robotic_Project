set(HEADERS
  occupancy_grid.h
  templateController.h
)

set(SOURCES
  templateController.cpp
  occupancy_grid.cpp
)

add_library(templateController MODULE ${HEADERS} ${SOURCES})

target_link_libraries(templateController
  argos3core_simulator
  argos3plugin_simulator_epuck
  argos3plugin_simulator_genericrobot)

