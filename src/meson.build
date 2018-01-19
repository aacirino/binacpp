project('binacpp lib', 'cpp', default_options : ['-std=c++11'])
jsoncpp_dep = dependency('jsoncpp', version : '>=1.8.3')
libcurl_dep = dependency('libcurl', version : '>=7.43.0')
libwebsockets_dep = dependency('libwebsockets', version : '>=2.4.0')
libcrypto_dep = dependency('libcrypto')
deps = [jsoncpp_dep, libcurl_dep, libwebsockets_dep, libcrypto_dep]
src = ['binacpp.cpp', 'binacpp_utils.cpp', 'binacpp_logger.cpp', 'binacpp_websocket.cpp']
hdr = ['binacpp.h', 'binacpp_utils.h', 'binacpp_logger.h', 'binacpp_websocket.h']
incdir = include_directories('/usr/include', '/usr/local/include')
install_headers(hdr, install_dir : '/usr/local/include/binacpp')
shared_library('binacpp', sources : src, version : '1.0', dependencies : deps, install : true, install_dir : '/usr/local/lib')
