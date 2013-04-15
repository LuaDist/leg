# Copyright (C) 2007-2013 LuaDist.
# Created by Peter Drahoš
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( leg NONE )
cmake_minimum_required ( VERSION 2.6 )
include ( cmake/dist.cmake )
include ( lua )

install_lua_module ( leg src/init.lua )
install_lua_module ( leg.grammar src/grammar.lua )
install_lua_module ( leg.parser src/parser.lua )
install_data ( README COPYRIGHT release )
install_doc ( doc/ )
install_test ( tests/ )
install_example ( examples/ )

add_lua_test ( tests/test.lua WORKING_DIRECTORY tests )
