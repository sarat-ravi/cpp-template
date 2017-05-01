BOOST_TARBALL=boost_1_60_0.tar.bz2
CPU_COUNT=4

.PHONY: default
default: build

boost_1_60_0: ${BOOST_TARBALL}
	tar -xjf ${BOOST_TARBALL}

build: boost_1_60_0
	cd boost_1_60_0 && ./bootstrap.sh --prefix=../build && ./b2 cxxflags=-fvisibility=hidden -j ${CPU_COUNT} threading=multi link=static --with-log --with-locale --with-program_options --with-test --with-serialization --with-iostreams install

