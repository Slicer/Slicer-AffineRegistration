cmake_minimum_required(VERSION 2.8.9)

project(AffineRegistration)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://wiki.slicer.org/slicerWiki/index.php/Documentation/Nightly/Modules/AffineRegistration")
set(EXTENSION_CATEGORY "Legacy.Registration")
set(EXTENSION_CONTRIBUTORS "Daniel Blezek (GE)")
set(EXTENSION_DESCRIPTION "Registers two images together using an affine transform and mutual information. This module is often used to align images of different subjects or images of the same subject from different modalities.\n\nThis module can smooth images prior to registration to mitigate noise and improve convergence. Many of the registration parameters require a working knowledge of the algorithm although the default parameters are sufficient for many registration tasks.\n\n")
set(EXTENSION_ICONURL "")
set(EXTENSION_SCREENSHOTURLS "")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(AffineRegistration)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
