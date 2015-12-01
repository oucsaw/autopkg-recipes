# Wireshark downloads

The goal of this recipe is to have a single wireshark download recipe,
which can take either a stable or development argument and download
the latest version of either stable or development branch for OSX.

The recipe takes the following inputs:

  NAME: name of download, default: Wireshark
  RELEASE: name of release to download, default: Stable
  ARCH: architecture default: Intel 64

The idea behind this recipe is that the download page has 'sections'
for each different release with headings that look like:

   %RELEASE% Release (version)

and then the download links look like:

  https://server/path/Wireshark %version% %ARCH%.dmg

The regular expression should match firstly the section heading to get
the version, and then using the version and architecture pick up the
correct link.

Currently the download page has the following releases:
   * Stable
   * Old Stable
However, in the not to distant past there has also been the
'Development' release.


