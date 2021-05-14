cmake_minimum_required(VERSION 3.2 FATAL_ERROR)
project(rxcpptests LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "-pthread")

add_executable(rxcpptests
                test.h
                catch.hpp all.cpp amb.cpp as_dynamic.cpp blocking_observable.cpp buffer.cpp combine_latest.cpp composite_exception.cpp
                concat.cpp concat_map.cpp contains.cpp create.cpp debounce.cpp default_if_empty.cpp defer.cpp delay.cpp
                distinct.cpp distinct_until_changed.cpp element_at.cpp empty.cpp error.cpp exists.cpp filter.cpp finally.cpp
                flat_map.cpp from.cpp group_by.cpp ignore_elements.cpp interval.cpp is_empty.cpp iterate.cpp just.cpp
                map.cpp math.cpp merge.cpp merge_delay_error.cpp never.cpp observe_on.cpp on_error_resume_next.cpp pairwise.cpp
                publish.cpp range.cpp reduce.cpp ref_count.cpp repeat.cpp replay.cpp retry.cpp sample.cpp scan.cpp scope.cpp
                sequence_equal.cpp skip.cpp skip_last.cpp skip_until.cpp skip_while.cpp start_with.cpp subscribe.cpp subscribe_on.cpp
                switch_if_empty.cpp switch_on_next.cpp take.cpp take_last.cpp take_until.cpp take_while.cpp tap.cpp time_interval.cpp
                timeout.cpp timer.cpp timestamp.cpp window.cpp with_latest_from.cpp zip.cpp
        )

find_package(rxcpp CONFIG)
find_package(Catch2 REQUIRED)