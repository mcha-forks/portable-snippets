# SPDX-FileCopyrightText: (C) 2025 Zephyr Lykos <self@mochaa.ws>
# SPDX-License-Identifier: 0BSD

project(
  'portable-snippets',
  'c',
  version: '0',
  license: 'CC0-1.0',
  default_options: [
    'c_std=gnu11,c18,c11,gnu99,c99,gnu89,c89',
    'warning_level=3',
  ],
)

inc = include_directories('.')

psnip_lib = library(
  'psnip',
  'cpu/cpu.c',
  'random/random.c',
  implicit_include_directories: false,
  include_directories: inc,
)

psnip_dep = declare_dependency(
  include_directories: inc,
  link_with: psnip_lib,
)
meson.override_dependency('psnip', psnip_dep)
