cmake_minimum_required(VERSION 4.3)
project(OpenGL)
string(JOIN "\n" EXT2
  "find_package(OpenGL REQUIRED BYPASS_PROVIDER)"
  "list(APPEND reqVars OpenGL_FOUND)"
  ""
  )
string(JOIN "\n" COND_OPEN
  ""
  "if(NOT DEFINED __xp_opengl_found_message_shown)"
  )
string(JOIN "\n" COND_CLOSE
  ""
  "  set(__xp_opengl_found_message_shown TRUE CACHE INTERNAL \"Flag to track if OpenGL found message was shown\")"
  "endif()"
  )
xpExternPackage(BASE v0 XPDIFF "bin"
  WEB "https://cmake.org/cmake/help/latest/module/FindOpenGL.html"
  DESC "Finds the OpenGL and OpenGL Utility Library (GLU)"
  LICENSE "[SGI-OpenGL](https://spdx.org/licenses/SGI-OpenGL.html 'SGI OpenGL License')"
  )
