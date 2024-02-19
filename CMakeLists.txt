cmake_minimum_required(VERSION 3.0)

# Define custom target for installation
add_custom_target(install_requirements
    COMMAND pip3 install -r requirements.txt
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
    COMMENT "Installing Python requirements"
)

# Define custom target for testing
add_custom_target(run_tests
    COMMAND pytest test.py
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
    COMMENT "Running tests"
)
