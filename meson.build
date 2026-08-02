project('life_sim', 'cpp',
  version : '0.1',
  default_options : [
    'cpp_std=c++20',
    'default_library=static',
    'b_vscrt=mdd'
  ]
)

sfml_proj = subproject('sfml', default_options : [
  'audio=false',
  'network=false',
  'graphics=true',
  'window=true'
])

sfml_dep = sfml_proj.get_variable('sfml_dep')
imgui_sfml_dep = dependency('imgui-sfml')

executable('life_sim',
  files('main.cpp'),
  dependencies : [
    sfml_dep,
    imgui_sfml_dep
  ]
)