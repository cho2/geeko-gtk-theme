AC_INIT(
    [geeko-theme],
    [20161119],
    [https://github.com/LelCP/geeko-theme/issues],
    [geeko-theme],
    [https://github.com/LelCP/geeko-theme],
    []
)

AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([no-dist-gzip dist-xz foreign])
AC_PROG_MKDIR_P

GEEKO_ENABLE([LIGHT],         [light],         [Geeko Light],     [disable])
GEEKO_ENABLE([DARKER],        [darker],        [Geeko Darker],    [disable])
GEEKO_ENABLE([DARK],          [dark],          [Geeko Dark],      [disable])
GEEKO_ENABLE([CINNAMON],      [cinnamon],      [Cinnamon],      [disable])
GEEKO_ENABLE([GNOME_SHELL],   [gnome-shell],   [GNOME Shell],   [disable])
GEEKO_ENABLE([GTK2],          [gtk2],          [GTK2],          [disable])
GEEKO_ENABLE([GTK3],          [gtk3],          [GTK3],          [disable])
GEEKO_ENABLE([METACITY],      [metacity],      [Metacity],      [disable])
GEEKO_ENABLE([UNITY],         [unity],         [Unity],         [disable])
GEEKO_ENABLE([XFWM],          [xfwm],          [XFWM],          [disable])
GEEKO_ENABLE([TRANSPARENCY],  [transparency],  [transparency],  [disable])

AS_IF([test "x$ENABLE_GNOME_SHELL$ENABLE_GTK3" != xnono], [GEEKO_GNOME])

AC_CONFIG_FILES([
    common/Makefile
    Makefile
])

AC_OUTPUT
