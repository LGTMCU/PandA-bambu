#this is file src/HLS/architecture_creation/controller_creation/Makefile.am
METASOURCES = AUTO

noinst_LTLIBRARIES =  lib_controller_creation.la

lib_controller_creation_la_CPPFLAGS = \
   -I$(top_srcdir)/src \
   -I$(top_srcdir)/src/behavior \
   -I$(top_srcdir)/src/circuit \
   -I$(top_srcdir)/src/constants \
   -I$(top_srcdir)/src/design_flows \
   -I$(top_srcdir)/src/graph \
   -I$(top_srcdir)/src/HLS \
   -I$(top_srcdir)/src/HLS/module_allocation \
   -I$(top_srcdir)/src/HLS/virtual_components \
   -I$(top_srcdir)/src/HLS/binding \
   -I$(top_srcdir)/src/HLS/binding/interconnection \
   -I$(top_srcdir)/src/HLS/binding/module \
   -I$(top_srcdir)/src/HLS/binding/register \
   -I$(top_srcdir)/src/HLS/scheduling \
   -I$(top_srcdir)/src/HLS/stg \
   -I$(top_srcdir)/src/intermediate_representations \
   -I$(top_srcdir)/src/intermediate_representations/hls \
   -I$(top_srcdir)/src/polixml \
   -I$(top_srcdir)/src/technology \
   -I$(top_srcdir)/src/technology/physical_library \
   -I$(top_srcdir)/src/technology/physical_library/models \
   -I$(top_srcdir)/src/technology/target_device \
   -I$(top_srcdir)/src/tree \
   -I$(top_srcdir)/src/utility \
   -I$(BOOST_DIR) $(all_includes)


noinst_HEADERS = \
   controller_creator_base_step.hpp fsm_controller.hpp

lib_controller_creation_la_SOURCES = \
   controller_creator_base_step.cpp fsm_controller.cpp

if BUILD_LIB_EXPERIMENTAL
  lib_controller_creation_la_CPPFLAGS += \
   -I$(top_srcdir)/src/algorithms/boolean_functions \
   -I$(top_srcdir)/src/algorithms/graph_helpers \
   -I$(top_srcdir)/src/algorithms/loops_detection \
   -I$(top_srcdir)/src/bdd \
   -I$(top_srcdir)/src/circuit/aig \
   -I$(top_srcdir)/src/HLS/chaining  \
   -I$(top_srcdir)/src/HLS/liveness


   noinst_HEADERS += ParallelController.hpp
   lib_controller_creation_la_SOURCES += ParallelController.cpp
endif

#DOCUMENTATION STUFF
PRJ_DOC = controller.doc fsm.doc
EXTRA_DIST = $(PRJ_DOC)

#do not touch the following line

