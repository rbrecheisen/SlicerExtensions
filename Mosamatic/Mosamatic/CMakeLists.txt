cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(Mosamatic)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/Mosamatic")
set(EXTENSION_CATEGORY "Mosamatic")
set(EXTENSION_CONTRIBUTORS "Ralph Brecheisen (Maastricht University)")
set(EXTENSION_DESCRIPTION "This is an extension for body composition analysis of CT images taken at the 3rd lumbar vertebral level")
set(EXTENSION_ICONURL "https://www.example.com/Slicer/Extensions/Mosamatic.png")
set(EXTENSION_SCREENSHOTURLS "https://www.example.com/Slicer/Extensions/Mosamatic/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(MuscleFatSegmentation)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
