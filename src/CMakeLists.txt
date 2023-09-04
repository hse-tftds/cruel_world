# Sandbox executable
add_executable(sandbox sandbox.cpp)
target_compile_features(sandbox PRIVATE cxx_std_20)
target_compile_options(sandbox PRIVATE -Wall -Wextra -Wpedantic)
target_link_libraries(sandbox PRIVATE fmt STDEXEC::stdexec)
# ASAN
target_compile_options(sandbox PRIVATE -fsanitize=address)
target_link_options(sandbox PRIVATE -fsanitize=address)
