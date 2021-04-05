# Needs CMake 3.14 or above
include(FetchContent)

# -------------------------------------------------------------------
# Catch2
FetchContent_Declare(Catch2
        GIT_REPOSITORY https://github.com/catchorg/Catch2.git
        GIT_TAG v2.13.4)

FetchContent_MakeAvailable(Catch2)
