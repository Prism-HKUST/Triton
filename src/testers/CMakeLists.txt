# These following tests are used to test our semantics. It relies on Unicorn emulator.
# We test our semantics on Linux and OSX only because the setup is easier.
if((${CMAKE_SYSTEM_NAME} MATCHES "Linux" OR ${CMAKE_SYSTEM_NAME} MATCHES "Darwin") AND PYTHON_BINDINGS)
    enable_testing()

    add_test(NAME UnicornAArch64Semantics   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/aarch64/unicorn_test_aarch64.py)
    add_test(NAME UnicornX86Semantics       COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/x86/unicorn_test_x86.py)
    add_test(NAME UnicornARM32Semantics1    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_branch_arm_1.py)
    add_test(NAME UnicornARM32Semantics2    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_branch_arm_2.py)
    add_test(NAME UnicornARM32Semantics3    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_branch_pc_arm_1.py)
    add_test(NAME UnicornARM32Semantics4    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_branch_pc_arm_2.py)
    add_test(NAME UnicornARM32Semantics5    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_branch_thumb_1.py)
    add_test(NAME UnicornARM32Semantics6    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_branch_thumb_2.py)
    add_test(NAME UnicornARM32Semantics7    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_data_arm.py)
    add_test(NAME UnicornARM32Semantics8    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_data_thumb.py)
    add_test(NAME UnicornARM32Semantics9    COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_interworking_arm_1.py)
    add_test(NAME UnicornARM32Semantics10   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_interworking_arm_2.py)
    add_test(NAME UnicornARM32Semantics11   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_interworking_thumb.py)
    add_test(NAME UnicornARM32Semantics12   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_it_thumb.py)
    add_test(NAME UnicornARM32Semantics13   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_arm_1.py)
    add_test(NAME UnicornARM32Semantics14   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_arm_2.py)
    add_test(NAME UnicornARM32Semantics15   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_arm_3.py)
    add_test(NAME UnicornARM32Semantics16   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_arm_4.py)
    add_test(NAME UnicornARM32Semantics17   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_arm_5.py)
    add_test(NAME UnicornARM32Semantics18   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_thumb_1.py)
    add_test(NAME UnicornARM32Semantics19   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_thumb_2.py)
    add_test(NAME UnicornARM32Semantics20   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_thumb_3.py)
    add_test(NAME UnicornARM32Semantics21   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/unicorn_test_arm32_loadstore_thumb_5.py)
    add_test(NAME UnicornARM32Semantics22   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-nothumb-O0-run.py)
    add_test(NAME UnicornARM32Semantics23   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-nothumb-O1-run.py)
    add_test(NAME UnicornARM32Semantics24   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-nothumb-O2-run.py)
    add_test(NAME UnicornARM32Semantics25   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-nothumb-O3-run.py)
    add_test(NAME UnicornARM32Semantics26   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-nothumb-Os-run.py)
    add_test(NAME UnicornARM32Semantics27   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-nothumb-Oz-run.py)
    add_test(NAME UnicornARM32Semantics28   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-thumb-O0-run.py)
    add_test(NAME UnicornARM32Semantics29   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-thumb-O1-run.py)
    add_test(NAME UnicornARM32Semantics30   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-thumb-O2-run.py)
    add_test(NAME UnicornARM32Semantics31   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-thumb-O3-run.py)
    add_test(NAME UnicornARM32Semantics32   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-thumb-Os-run.py)
    add_test(NAME UnicornARM32Semantics33   COMMAND ${PYTHON_EXECUTABLE} ${CMAKE_CURRENT_LIST_DIR}/arm32/crypto_test/crypto_test-thumb-Oz-run.py)

    set_property(TEST
        UnicornAArch64Semantics
        UnicornX86Semantics
        UnicornARM32Semantics1
        UnicornARM32Semantics2
        UnicornARM32Semantics3
        UnicornARM32Semantics4
        UnicornARM32Semantics5
        UnicornARM32Semantics6
        UnicornARM32Semantics7
        UnicornARM32Semantics8
        UnicornARM32Semantics9
        UnicornARM32Semantics10
        UnicornARM32Semantics11
        UnicornARM32Semantics12
        UnicornARM32Semantics13
        UnicornARM32Semantics14
        UnicornARM32Semantics15
        UnicornARM32Semantics16
        UnicornARM32Semantics17
        UnicornARM32Semantics18
        UnicornARM32Semantics19
        UnicornARM32Semantics20
        UnicornARM32Semantics21
        UnicornARM32Semantics22
        UnicornARM32Semantics23
        UnicornARM32Semantics24
        UnicornARM32Semantics25
        UnicornARM32Semantics26
        UnicornARM32Semantics27
        UnicornARM32Semantics28
        UnicornARM32Semantics29
        UnicornARM32Semantics30
        UnicornARM32Semantics31
        UnicornARM32Semantics32
        UnicornARM32Semantics33
        PROPERTY ENVIRONMENT "PYTHONPATH=$<TARGET_FILE_DIR:triton>"
    )
endif()
