cmake_minimum_required(VERSION 3.10)

project(demo)

set(EXAMPLES
        LBRClientTemplate
        LBRJointSineOverlay
        LBRTorqueSineOverlay
        LBRWrenchSineOverlay
)

foreach(EXAMPLE ${EXAMPLES})
    add_subdirectory(${EXAMPLE})
endforeach(EXAMPLE)

