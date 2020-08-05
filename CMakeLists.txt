cmake_minimum_required(VERSION 3.17)
project(rfc5769check C)

set(CMAKE_C_STANDARD 99)

link_libraries(rt)
link_libraries(nsl)
link_libraries(resolv)
link_libraries(pthread)
link_libraries(crypto)
link_libraries(ssl)
link_libraries(event_core)
link_libraries(event_extra)
link_libraries(event_openssl)
link_libraries(event_pthreads)


add_executable(rfc5769check rfc5769check.c src/apputils.c src/apputils.h src/ns_turn_defs.h src/ns_turn_ioalib.h src/ns_turn_msg.h src/ns_turn_msg.c src/ns_turn_ioaddr.c src/ns_turn_msg_addr.h src/ns_turn_msg_addr.c src/ns_turn_msg_addr.h src/ns_turn_defs.h src/ns_turn_msg_defs_experimental.h src/ns_turn_openssl.h src/ns_turn_utils.c src/ns_turn_utils.h src/stun_buffer.c src/stun_buffer.h)