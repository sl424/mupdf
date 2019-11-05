##Download

The latest development source is available directly from the git repository:

	git clone --recursive https://github.com/sl424/mupdf

In the mupdf directory, update the third party libraries:

	git submodule update --init

Compiling on Linux

If you are compiling from source you will need several third party libraries: freetype2, jbig2dec, libjpeg, openjpeg, and zlib. These libraries are contained in the source archive. If you are using git, they are included as git submodules.

You will also need the X11 headers and libraries if you're building on Linux. These can typically be found in the xorg-dev package. Alternatively, if you only want the command line tools, you can build with HAVE_X11=no.

The new OpenGL-based viewer also needs OpenGL headers and libraries. If you're building on Linux, install the mesa-common-dev, libgl1-mesa-dev packages, and libglu1-mesa-dev packages. You'll also need several X11 development packages: xorg-dev, libxcursor-dev, libxrandr-dev, and libxinerama-dev. To skip building the OpenGL viewer, build with HAVE_GLUT=no.

To install the viewer, command line tools, libraries, and header files on your system:

	make prefix=/usr/local install

To install only opengl:

	make HAVE_X11=no prefix=/usr/local install
	
To install only the command line tools, libraries, and headers invoke make like this:

	make HAVE_X11=no HAVE_GLUT=no prefix=/usr/local install

##ABOUT

MuPDF is a lightweight open source software framework for viewing and converting
PDF, XPS, and E-book documents.

See the documentation in docs/index.html for an overview.

Build instructions can be found in docs/building.html.

LICENSE

MuPDF is Copyright (c) 2006-2017 Artifex Software, Inc.

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU Affero General Public License as published by the Free
Software Foundation, either version 3 of the License, or (at your option) any
later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU Affero General Public License along
with this program. If not, see <http://www.gnu.org/licenses/>.

For commercial licensing, including our "Indie Dev" friendly options,
please contact sales@artifex.com.

REPORTING BUGS AND PROBLEMS

The MuPDF developers hang out on IRC in the #mupdf channel on irc.freenode.net.

Report bugs on the ghostscript bugzilla, with MuPDF as the selected component.

	http://bugs.ghostscript.com/

If you are reporting a problem with a specific file, please include the file as
an attachment.
