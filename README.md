CallStack in gen7:

...
intel_get_renderbuffer (attIndex=BUFFER_DEPTH, fb=0x782e40) at intel_fbo.h:173
intel_renderbuffer (rb=0x615970) at intel_fbo.h:143
brw_fast_clear_depth (ctx=ctx@entry=0x7ffff7fa6040) at brw_clear.c:108
intel_renderbuffer_has_hiz (irb=irb@entry=0x615970) at intel_fbo.c:964
intel_miptree_level_has_hiz (mt=0x7836d0, level=0) at intel_mipmap_tree.c:2053
intel_miptree_check_level_layer (mt=mt@entry=0x7836d0, level=level@entry=0, layer=layer@entry=0) at intel_mipmap_tree.c:657
intel_miptree_level_has_hiz (mt=0x7836d0, level=0) at intel_mipmap_tree.c:2055
intel_renderbuffer_has_hiz (irb=irb@entry=0x615970) at intel_fbo.c:966
brw_fast_clear_depth (ctx=ctx@entry=0x7ffff7fa6040) at brw_clear.c:121
intel_miptree_prepare_access (brw=brw@entry=0x7ffff7fa6040, mt=mt@entry=0x7836d0, start_level=start_level@entry=0, num_levels=num_levels@entry=4294967295, start_layer=start_layer@entry=0, num_layers=num_layers@entry=4294967295, aux_supported=true, fast_clear_supported=false)
    at intel_mipmap_tree.c:2434
miptree_level_range_length (num_levels=4294967295, start_level=0, mt=0x7836d0) at intel_mipmap_tree.c:2392
intel_miptree_prepare_access (brw=brw@entry=0x7ffff7fa6040, mt=mt@entry=0x7836d0, start_level=start_level@entry=0, num_levels=<optimized out>, num_levels@entry=4294967295, start_layer=start_layer@entry=0, num_layers=num_layers@entry=4294967295, aux_supported=true,
    fast_clear_supported=false) at intel_mipmap_tree.c:2437
_mesa_is_format_color_format (format=MESA_FORMAT_Z24_UNORM_X8_UINT) at main/formats.c:574
_mesa_get_format_info (format=MESA_FORMAT_Z24_UNORM_X8_UINT) at main/formats.c:85
_mesa_is_format_color_format (format=<optimized out>) at main/formats.c:576
intel_miptree_prepare_access (brw=brw@entry=0x7ffff7fa6040, mt=mt@entry=0x7836d0, start_level=start_level@entry=0, num_levels=<optimized out>, num_levels@entry=4294967295, start_layer=start_layer@entry=0, num_layers=num_layers@entry=4294967295, aux_supported=true,
    fast_clear_supported=false) at intel_mipmap_tree.c:2456
intel_miptree_level_has_hiz (mt=mt@entry=0x7836d0, level=level@entry=0) at intel_mipmap_tree.c:2053
intel_miptree_check_level_layer (mt=mt@entry=0x7836d0, level=level@entry=0, layer=layer@entry=0) at intel_mipmap_tree.c:657
intel_miptree_level_has_hiz (mt=mt@entry=0x7836d0, level=level@entry=0) at intel_mipmap_tree.c:2055
intel_miptree_prepare_access (brw=brw@entry=0x7ffff7fa6040, mt=mt@entry=0x7836d0, start_level=start_level@entry=0, num_levels=<optimized out>, num_levels@entry=4294967295, start_layer=start_layer@entry=0, num_layers=num_layers@entry=4294967295, aux_supported=true,
    fast_clear_supported=false) at intel_mipmap_tree.c:2467
miptree_layer_range_length (num_layers=4294967295, start_layer=0, level=0, mt=0x7836d0) at intel_mipmap_tree.c:2408
intel_miptree_prepare_hiz_access (brw=brw@entry=0x7ffff7fa6040, mt=mt@entry=0x7836d0, level=level@entry=0, layer=layer@entry=0, hiz_supported=hiz_supported@entry=true, fast_clear_supported=fast_clear_supported@entry=false) at intel_mipmap_tree.c:2302
intel_miptree_get_aux_state (mt=mt@entry=0x7836d0, level=level@entry=0, layer=layer@entry=0) at intel_mipmap_tree.c:2517
intel_miptree_check_level_layer (mt=mt@entry=0x7836d0, level=level@entry=0, layer=layer@entry=0) at intel_mipmap_tree.c:657
intel_miptree_get_aux_state (mt=mt@entry=0x7836d0, level=level@entry=0, layer=layer@entry=0) at intel_mipmap_tree.c:2520
_mesa_is_format_color_format (format=MESA_FORMAT_Z24_UNORM_X8_UINT) at main/formats.c:574
_mesa_get_format_info (format=MESA_FORMAT_Z24_UNORM_X8_UINT) at main/formats.c:85
_mesa_is_format_color_format (format=<optimized out>) at main/formats.c:576
intel_hiz_exec (brw=brw@entry=0x7ffff7fa6040, mt=mt@entry=0x7836d0, level=level@entry=0, start_layer=start_layer@entry=0, num_layers=num_layers@entry=1, op=op@entry=BLORP_HIZ_OP_HIZ_RESOLVE) at brw_blorp.c:1076
intel_miptree_level_has_hiz (mt=mt@entry=0x7836d0, level=level@entry=0) at intel_mipmap_tree.c:2053
intel_miptree_check_level_layer (mt=mt@entry=0x7836d0, level=level@entry=0, layer=layer@entry=0) at intel_mipmap_tree.c:657
intel_miptree_level_has_hiz (mt=mt@entry=0x7836d0, level=level@entry=0) at intel_mipmap_tree.c:2055
intel_hiz_exec (brw=brw@entry=0x7ffff7fa6040, mt=mt@entry=0x7836d0, level=level@entry=0, start_layer=start_layer@entry=0, num_layers=num_layers@entry=1, op=op@entry=BLORP_HIZ_OP_HIZ_RESOLVE) at brw_blorp.c:1078
brw_emit_pipe_control_flush (brw=brw@entry=0x7ffff7fa6040, flags=flags@entry=1048577) at brw_pipe_control.c:175
brw_emit_pipe_control (brw=brw@entry=0x7ffff7fa6040, flags=flags@entry=1048577, bo=bo@entry=0x0, offset=offset@entry=0, imm=imm@entry=0) at brw_pipe_control.c:93
gen7_cs_stall_every_four_pipe_controls (brw=brw@entry=0x7ffff7fa6040, flags=1048577) at brw_pipe_control.c:74
brw_emit_pipe_control (brw=brw@entry=0x7ffff7fa6040, flags=flags@entry=1048577, bo=bo@entry=0x0, offset=offset@entry=0, imm=imm@entry=0) at brw_pipe_control.c:138
intel_batchbuffer_begin (ring=RENDER_RING, n=5, brw=0x7ffff7fa6040) at intel_batchbuffer.h:137
intel_batchbuffer_require_space (brw=brw@entry=0x7ffff7fa6040, sz=sz@entry=20, ring=ring@entry=RENDER_RING) at intel_batchbuffer.c:176
intel_batchbuffer_space (batch=0x7ffff7fcb0e8) at intel_batchbuffer.h:113
intel_batchbuffer_require_space (brw=brw@entry=0x7ffff7fa6040, sz=sz@entry=20, ring=ring@entry=RENDER_RING) at intel_batchbuffer.c:186
...
