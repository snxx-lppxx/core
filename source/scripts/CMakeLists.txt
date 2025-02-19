# Check if scripts are enabled
if(NOT OPTION_BUILD_SCRIPTS)
	return()
endif()

if(NOT LOADER_SCRIPT_PATH)
	return()
endif()

# Create output directory
file(MAKE_DIRECTORY ${LOADER_SCRIPT_PATH})

# Plugins options
option(OPTION_BUILD_SCRIPTS_C "Build C scripts." ON)
option(OPTION_BUILD_SCRIPTS_COB "Build Cobol scripts." ON)
option(OPTION_BUILD_SCRIPTS_CS "Build C# scripts." ON)
option(OPTION_BUILD_SCRIPTS_FILE "Build File scripts." ON)
option(OPTION_BUILD_SCRIPTS_JAVA "Build Java scripts." ON)
option(OPTION_BUILD_SCRIPTS_JL "Build Julia scripts." ON)
option(OPTION_BUILD_SCRIPTS_JS "Build JavaScript scripts." ON)
option(OPTION_BUILD_SCRIPTS_LLVM "Build LLVM scripts." ON)
option(OPTION_BUILD_SCRIPTS_LUA "Build Lua scripts." ON)
option(OPTION_BUILD_SCRIPTS_NODE "Build NodeJS scripts." ON)
option(OPTION_BUILD_SCRIPTS_PY "Build Python scripts." ON)
option(OPTION_BUILD_SCRIPTS_RB "Build Ruby scripts." ON)
option(OPTION_BUILD_SCRIPTS_RS "Build Rust scripts." ON)
option(OPTION_BUILD_SCRIPTS_RPC "Build RPC scripts." ON)
option(OPTION_BUILD_SCRIPTS_TS "Build TypeScript scripts." ON)
option(OPTION_BUILD_SCRIPTS_WASM "Build WebAssembly scripts." ON)

# Script directory packages
add_subdirectory(c)
add_subdirectory(cobol)
add_subdirectory(csharp)
add_subdirectory(file)
add_subdirectory(java)
add_subdirectory(julia)
add_subdirectory(javascript)
add_subdirectory(llvm)
add_subdirectory(node)
add_subdirectory(python)
add_subdirectory(ruby)
add_subdirectory(rust)
add_subdirectory(rpc)
add_subdirectory(typescript)
add_subdirectory(wasm)
