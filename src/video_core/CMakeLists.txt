add_subdirectory(host_shaders)

add_library(video_core STATIC
    buffer_cache/buffer_base.h
    buffer_cache/buffer_block.h
    buffer_cache/buffer_cache.h
    buffer_cache/map_interval.cpp
    buffer_cache/map_interval.h
    cdma_pusher.cpp
    cdma_pusher.h
    command_classes/codecs/codec.cpp
    command_classes/codecs/codec.h
    command_classes/codecs/h264.cpp
    command_classes/codecs/h264.h
    command_classes/codecs/vp9.cpp
    command_classes/codecs/vp9.h
    command_classes/codecs/vp9_types.h
    command_classes/host1x.cpp
    command_classes/host1x.h
    command_classes/nvdec.cpp
    command_classes/nvdec.h
    command_classes/nvdec_common.h
    command_classes/sync_manager.cpp
    command_classes/sync_manager.h
    command_classes/vic.cpp
    command_classes/vic.h
    compatible_formats.cpp
    compatible_formats.h
    delayed_destruction_ring.h
    dirty_flags.cpp
    dirty_flags.h
    dma_pusher.cpp
    dma_pusher.h
    engines/const_buffer_engine_interface.h
    engines/const_buffer_info.h
    engines/engine_interface.h
    engines/engine_upload.cpp
    engines/engine_upload.h
    engines/fermi_2d.cpp
    engines/fermi_2d.h
    engines/kepler_compute.cpp
    engines/kepler_compute.h
    engines/kepler_memory.cpp
    engines/kepler_memory.h
    engines/maxwell_3d.cpp
    engines/maxwell_3d.h
    engines/maxwell_dma.cpp
    engines/maxwell_dma.h
    engines/shader_bytecode.h
    engines/shader_header.h
    engines/shader_type.h
    framebuffer_config.h
    macro/macro.cpp
    macro/macro.h
    macro/macro_hle.cpp
    macro/macro_hle.h
    macro/macro_interpreter.cpp
    macro/macro_interpreter.h
    macro/macro_jit_x64.cpp
    macro/macro_jit_x64.h
    fence_manager.h
    gpu.cpp
    gpu.h
    gpu_thread.cpp
    gpu_thread.h
    guest_driver.cpp
    guest_driver.h
    memory_manager.cpp
    memory_manager.h
    morton.cpp
    morton.h
    query_cache.h
    rasterizer_accelerated.cpp
    rasterizer_accelerated.h
    rasterizer_interface.h
    renderer_base.cpp
    renderer_base.h
    renderer_opengl/gl_arb_decompiler.cpp
    renderer_opengl/gl_arb_decompiler.h
    renderer_opengl/gl_buffer_cache.cpp
    renderer_opengl/gl_buffer_cache.h
    renderer_opengl/gl_device.cpp
    renderer_opengl/gl_device.h
    renderer_opengl/gl_fence_manager.cpp
    renderer_opengl/gl_fence_manager.h
    renderer_opengl/gl_rasterizer.cpp
    renderer_opengl/gl_rasterizer.h
    renderer_opengl/gl_resource_manager.cpp
    renderer_opengl/gl_resource_manager.h
    renderer_opengl/gl_shader_cache.cpp
    renderer_opengl/gl_shader_cache.h
    renderer_opengl/gl_shader_decompiler.cpp
    renderer_opengl/gl_shader_decompiler.h
    renderer_opengl/gl_shader_disk_cache.cpp
    renderer_opengl/gl_shader_disk_cache.h
    renderer_opengl/gl_shader_manager.cpp
    renderer_opengl/gl_shader_manager.h
    renderer_opengl/gl_shader_util.cpp
    renderer_opengl/gl_shader_util.h
    renderer_opengl/gl_state_tracker.cpp
    renderer_opengl/gl_state_tracker.h
    renderer_opengl/gl_stream_buffer.cpp
    renderer_opengl/gl_stream_buffer.h
    renderer_opengl/gl_texture_cache.cpp
    renderer_opengl/gl_texture_cache.h
    renderer_opengl/gl_query_cache.cpp
    renderer_opengl/gl_query_cache.h
    renderer_opengl/maxwell_to_gl.h
    renderer_opengl/renderer_opengl.cpp
    renderer_opengl/renderer_opengl.h
    renderer_opengl/util_shaders.cpp
    renderer_opengl/util_shaders.h
    renderer_vulkan/blit_image.cpp
    renderer_vulkan/blit_image.h
    renderer_vulkan/fixed_pipeline_state.cpp
    renderer_vulkan/fixed_pipeline_state.h
    renderer_vulkan/maxwell_to_vk.cpp
    renderer_vulkan/maxwell_to_vk.h
    renderer_vulkan/renderer_vulkan.h
    renderer_vulkan/renderer_vulkan.cpp
    renderer_vulkan/vk_blit_screen.cpp
    renderer_vulkan/vk_blit_screen.h
    renderer_vulkan/vk_buffer_cache.cpp
    renderer_vulkan/vk_buffer_cache.h
    renderer_vulkan/vk_command_pool.cpp
    renderer_vulkan/vk_command_pool.h
    renderer_vulkan/vk_compute_pass.cpp
    renderer_vulkan/vk_compute_pass.h
    renderer_vulkan/vk_compute_pipeline.cpp
    renderer_vulkan/vk_compute_pipeline.h
    renderer_vulkan/vk_descriptor_pool.cpp
    renderer_vulkan/vk_descriptor_pool.h
    renderer_vulkan/vk_fence_manager.cpp
    renderer_vulkan/vk_fence_manager.h
    renderer_vulkan/vk_graphics_pipeline.cpp
    renderer_vulkan/vk_graphics_pipeline.h
    renderer_vulkan/vk_master_semaphore.cpp
    renderer_vulkan/vk_master_semaphore.h
    renderer_vulkan/vk_pipeline_cache.cpp
    renderer_vulkan/vk_pipeline_cache.h
    renderer_vulkan/vk_query_cache.cpp
    renderer_vulkan/vk_query_cache.h
    renderer_vulkan/vk_rasterizer.cpp
    renderer_vulkan/vk_rasterizer.h
    renderer_vulkan/vk_resource_pool.cpp
    renderer_vulkan/vk_resource_pool.h
    renderer_vulkan/vk_scheduler.cpp
    renderer_vulkan/vk_scheduler.h
    renderer_vulkan/vk_shader_decompiler.cpp
    renderer_vulkan/vk_shader_decompiler.h
    renderer_vulkan/vk_shader_util.cpp
    renderer_vulkan/vk_shader_util.h
    renderer_vulkan/vk_staging_buffer_pool.cpp
    renderer_vulkan/vk_staging_buffer_pool.h
    renderer_vulkan/vk_state_tracker.cpp
    renderer_vulkan/vk_state_tracker.h
    renderer_vulkan/vk_stream_buffer.cpp
    renderer_vulkan/vk_stream_buffer.h
    renderer_vulkan/vk_swapchain.cpp
    renderer_vulkan/vk_swapchain.h
    renderer_vulkan/vk_texture_cache.cpp
    renderer_vulkan/vk_texture_cache.h
    renderer_vulkan/vk_update_descriptor.cpp
    renderer_vulkan/vk_update_descriptor.h
    shader_cache.h
    shader_notify.cpp
    shader_notify.h
    shader/decode/arithmetic.cpp
    shader/decode/arithmetic_immediate.cpp
    shader/decode/bfe.cpp
    shader/decode/bfi.cpp
    shader/decode/shift.cpp
    shader/decode/arithmetic_integer.cpp
    shader/decode/arithmetic_integer_immediate.cpp
    shader/decode/arithmetic_half.cpp
    shader/decode/arithmetic_half_immediate.cpp
    shader/decode/ffma.cpp
    shader/decode/hfma2.cpp
    shader/decode/conversion.cpp
    shader/decode/memory.cpp
    shader/decode/texture.cpp
    shader/decode/image.cpp
    shader/decode/float_set_predicate.cpp
    shader/decode/integer_set_predicate.cpp
    shader/decode/half_set_predicate.cpp
    shader/decode/predicate_set_register.cpp
    shader/decode/predicate_set_predicate.cpp
    shader/decode/register_set_predicate.cpp
    shader/decode/float_set.cpp
    shader/decode/integer_set.cpp
    shader/decode/half_set.cpp
    shader/decode/video.cpp
    shader/decode/warp.cpp
    shader/decode/xmad.cpp
    shader/decode/other.cpp
    shader/ast.cpp
    shader/ast.h
    shader/async_shaders.cpp
    shader/async_shaders.h
    shader/compiler_settings.cpp
    shader/compiler_settings.h
    shader/control_flow.cpp
    shader/control_flow.h
    shader/decode.cpp
    shader/expr.cpp
    shader/expr.h
    shader/memory_util.cpp
    shader/memory_util.h
    shader/node_helper.cpp
    shader/node_helper.h
    shader/node.h
    shader/registry.cpp
    shader/registry.h
    shader/shader_ir.cpp
    shader/shader_ir.h
    shader/track.cpp
    shader/transform_feedback.cpp
    shader/transform_feedback.h
    surface.cpp
    surface.h
    texture_cache/accelerated_swizzle.cpp
    texture_cache/accelerated_swizzle.h
    texture_cache/decode_bc4.cpp
    texture_cache/decode_bc4.h
    texture_cache/descriptor_table.h
    texture_cache/formatter.cpp
    texture_cache/formatter.h
    texture_cache/format_lookup_table.cpp
    texture_cache/format_lookup_table.h
    texture_cache/image_base.cpp
    texture_cache/image_base.h
    texture_cache/image_info.cpp
    texture_cache/image_info.h
    texture_cache/image_view_base.cpp
    texture_cache/image_view_base.h
    texture_cache/image_view_info.cpp
    texture_cache/image_view_info.h
    texture_cache/render_targets.h
    texture_cache/samples_helper.h
    texture_cache/slot_vector.h
    texture_cache/texture_cache.h
    texture_cache/types.h
    texture_cache/util.cpp
    texture_cache/util.h
    textures/astc.cpp
    textures/astc.h
    textures/decoders.cpp
    textures/decoders.h
    textures/texture.cpp
    textures/texture.h
    video_core.cpp
    video_core.h
    vulkan_common/vulkan_debug_callback.cpp
    vulkan_common/vulkan_debug_callback.h
    vulkan_common/vulkan_device.cpp
    vulkan_common/vulkan_device.h
    vulkan_common/vulkan_instance.cpp
    vulkan_common/vulkan_instance.h
    vulkan_common/vulkan_library.cpp
    vulkan_common/vulkan_library.h
    vulkan_common/vulkan_memory_allocator.cpp
    vulkan_common/vulkan_memory_allocator.h
    vulkan_common/vulkan_surface.cpp
    vulkan_common/vulkan_surface.h
    vulkan_common/vulkan_wrapper.cpp
    vulkan_common/vulkan_wrapper.h
    vulkan_common/nsight_aftermath_tracker.cpp
    vulkan_common/nsight_aftermath_tracker.h
)

create_target_directory_groups(video_core)

target_link_libraries(video_core PUBLIC common core)
target_link_libraries(video_core PRIVATE glad xbyak)

if (MSVC)
    target_include_directories(video_core PRIVATE ${FFMPEG_INCLUDE_DIR})
    target_link_libraries(video_core PUBLIC ${FFMPEG_LIBRARY_DIR}/swscale.lib ${FFMPEG_LIBRARY_DIR}/avcodec.lib ${FFMPEG_LIBRARY_DIR}/avutil.lib)
else()
    target_include_directories(video_core PRIVATE ${FFMPEG_INCLUDE_DIR})
    target_link_libraries(video_core PRIVATE ${FFMPEG_LIBRARIES})
endif()

add_dependencies(video_core host_shaders)
target_include_directories(video_core PRIVATE ${HOST_SHADERS_INCLUDE})
target_include_directories(video_core PRIVATE sirit ../../externals/Vulkan-Headers/include)
target_link_libraries(video_core PRIVATE sirit)

if (ENABLE_NSIGHT_AFTERMATH)
    if (NOT DEFINED ENV{NSIGHT_AFTERMATH_SDK})
        message(ERROR "Environment variable NSIGHT_AFTERMATH_SDK has to be provided")
    endif()
    if (NOT WIN32)
        message(ERROR "Nsight Aftermath doesn't support non-Windows platforms")
    endif()
    target_compile_definitions(video_core PRIVATE HAS_NSIGHT_AFTERMATH)
    target_include_directories(video_core PRIVATE "$ENV{NSIGHT_AFTERMATH_SDK}/include")
endif()

if (MSVC)
    target_compile_options(video_core PRIVATE
        /we4267 # 'var' : conversion from 'size_t' to 'type', possible loss of data
        /we4456 # Declaration of 'identifier' hides previous local declaration
        /we4457 # Declaration of 'identifier' hides function parameter
        /we4458 # Declaration of 'identifier' hides class member
        /we4459 # Declaration of 'identifier' hides global declaration
        /we4715 # 'function' : not all control paths return a value
    )
else()
    target_compile_options(video_core PRIVATE
        -Werror=conversion
        -Wno-error=sign-conversion
        -Werror=pessimizing-move
        -Werror=redundant-move
        -Werror=shadow
        -Werror=type-limits

        $<$<CXX_COMPILER_ID:GNU>:-Werror=class-memaccess>
        $<$<CXX_COMPILER_ID:GNU>:-Werror=unused-but-set-parameter>
        $<$<CXX_COMPILER_ID:GNU>:-Werror=unused-but-set-variable>
    )
endif()
