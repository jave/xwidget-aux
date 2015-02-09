FROM debian:latest

# install things we need to build the emacsxwidget branch
RUN apt-get update
#RUN apt-get -y install git


RUN apt-get -y install build-essential libncurses5-dev texinfo liblockfile-dev librsvg2-dev libgif-dev libtiff-dev libpng-dev libjpeg-dev libm17n-dev libotf-dev libgpm-dev libdbus-1-dev autoconf automake autotools-dev imagemagick libgtk-3-dev libwebkitgtk-3.0-dev libgirepository1.0-dev libxpm-dev


#RUN git clone  --depth 1 -b xwidget git://git.savannah.gnu.org/emacs.git xwidget 

CMD	cd xwidget && git checkout xwidget &&		export CFLAGS=" -g" && ./autogen.sh &&  	./configure --with-xwidgets --with-x-toolkit=gtk3 && 	make -j4




