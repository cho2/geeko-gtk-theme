AC_INIT(
    [arc-geeko-theme],
    [20161119],
    [https://github.com/LelCP/geeko-theme/issues],
    [arc-geeko-theme],
    [https://github.com/LelCP/geeko-theme],
    []
)

AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([no-dist-gzip dist-xz foreign])
AC_PROG_MKDIR_P

ARC_GEEKO_ENABLE([LIGHT],         [light],         [Arc Geeko Light],     [disable])
ARC_GEEKO_ENABLE([DARKER],        [darker],        [Arc Geeko Darker],    [disable])
ARC_GEEKO_ENABLE([DARK],          [dark],          [Arc Geeko Dark],      [disable])
ARC_GEEKO_ENABLE([CINNAMON],      [cinnamon],      [Cinnamon],      [disable])
ARC_GEEKO_ENABLE([GNOME_SHELL],   [gnome-shell],   [GNOME Shell],   [disable])
ARC_GEEKO_ENABLE([GTK2],          [gtk2],          [GTK2],          [disable])
ARC_GEEKO_ENABLE([GTK3],          [gtk3],          [GTK3],          [disable])
ARC_GEEKO_ENABLE([METACITY],      [metacity],      [Metacity],      [disable])
ARC_GEEKO_ENABLE([UNITY],         [unity],         [Unity],         [disable])
ARC_GEEKO_ENABLE([XFWM],          [xfwm],          [XFWM],          [disable])
ARC_GEEKO_ENABLE([TRANSPARENCY],  [transparency],  [transparency],  [disable])

AS_IF([test "x$ENABLE_GNOME_SHELL$ENABLE_GTK3" != xnono], [ARC_GEEKO_GNOME])

AC_CONFIG_FILES([
    common/Makefile
    Makefile
])

AC_OUTPUT
