FROM fedora:20

# install things we need to build the emacsxwidget branch
RUN yum -y install git

RUN yum -y groupinstall "Development Tools"
RUN yum -y install gobject-introspection-devel webkitgtk3-devel libjpeg-turbo libXpm-devel libungif-devel libjpeg-devel libnsurses-devel texinfo libncurses-devel
RUN yum -y install libtiff-devel
RUN yum -y install ncurses-devel
RUN yum -y install  xorg-x11-apps #this is just for debugging

RUN git clone  --depth 1 -b xwidget git://git.savannah.gnu.org/emacs.git xwidget



RUN	cd xwidget && git checkout xwidget &&		export CFLAGS=" -g" && ./autogen.sh &&  	./configure --with-xwidgets --with-x-toolkit=gtk3 && 	make -j4




