manokwari_panel_sources = [
    'main.vala',
    'panel-abstract-window.vala',
    'panel-window.vala',
    'panel-menu-box.vala',
    'panel-menu-content.vala',
    'panel-tray.vala',
    'panel-scrollable-content.vala',
    'panel-animated-adjustment.vala',
    'panel-clock.vala',
    'panel-places.vala',
    'panel-screen.vala',
    'utils.vala',
    'panel-hotkey.vala',
    'panel-session-manager.vala',
    'panel-menu-html.vala',
    'xdg-data.vala',
    'panel-user.vala',
    'panel-desktop.vala',
    'panel-desktop-html.vala',
    'panel-desktop-data.vala',
    'panel-calendar.vala',
    'animated-property.vala',
    'panel-shell.vala',
    'panel-socket.vala',
    'panel-xdg-properties.vala',
]

manokwari_panel_deps = [
    dep_gtk3,
    dep_glib,
    dep_atk,
    dep_x11,
    dep_gee,
    dep_cairo,
    dep_libgnomemenu,
    dep_unique,
    dep_webkit,
    dep_libnotify,
    dep_libwnck,
]

manokwari_vapi = join_paths(meson.source_root(), 'vapi')

executable(
    'manokwari', manokwari_panel_sources,
    dependencies: manokwari_panel_deps,
    include_directories: extra_includes,
    vala_args: [
        '--pkg', 'config',
        '--vapidir', manokwari_vapi,
        '--pkg', 'atk',
        '--pkg', 'x11',
        '--pkg', 'gdk-x11-3.0',
        '--pkg', 'gee-1.0',
        '--pkg', 'cairo',
        '--pkg', 'gtk+-3.0',
        '--pkg', 'gio-unix-2.0',
        '--pkg', 'libgnome-menu-3.0',
        '--pkg', 'gdk-3.0',
        '--pkg', 'libwnck-3.0',
        '--pkg', 'unique-3.0',
        '--pkg', 'webkitgtk-3.0',
        '--pkg', 'javascriptcore',
        '--pkg', 'libsoup-2.4',
        '--pkg', 'libnotify',
    ],
    c_args: [
        '-DGMENU_I_KNOW_THIS_IS_UNSTABLE',
        '-DWNCK_I_KNOW_THIS_IS_UNSTABLE',
    ],
    install: true,
)
