OQS Integration Testing
=======================

The **Open Quantum Safe (OQS) project** has the goal of developing and prototyping quantum-resistant cryptography.  [liboqs](https://github.com/open-quantum-safe/liboqs) is an open source C library for post-quantum cryptographic algorithms.  The OQS project has developed forks of [OpenSSH](https://github.com/open-quantum-safe/openssh-portable) and [OpenSSL](https://github.com/open-quantum-safe/openssl) that integrate quantum-resistant algorithms into the SSH and TLS protocols.

This repository contains scripts for testing the integration of liboqs into OpenSSH and OpenSSL.  

Please check the README.md files under the integration/oqs-openssh and integration/oqs-openssl directories for details on how to run the respective tests.

OQS developers should record their test results on the OQS [test coverage wiki page](https://github.com/open-quantum-safe/testing/wiki/Configurations-test-coverage).

Dependencies
------------

You must install the relevant dependices before proceeding with running any tests.

**Debian/Ubuntu (apt)**

	sudo apt update
	sudo apt install build-essential autotools-dev autoconf git libssl-dev libtool xsltproc zlib1g-dev zip
	
On Ubuntu 14.04, you need to also:

	sudo add-apt-repository ppa:ubuntu-toolchain-r/test
	sudo apt update
	sudo apt install gcc-5

**Centos (yum)**

	sudo yum groupinstall 'Development Tools'
	sudo yum install centos-release-scl devtoolset-7-gcc-c++
	sudo scl enable devtoolset-7 bash
	sudo yum install libtool

**Amazon Linux 2 (yum)**

	sudo yum install automake gcc-c++ git libtool libxslt zlib-devel

**macOS (brew)**

	brew install autoconf automake libtool openssl wget

License
-------

This repository is licensed under the MIT License; see [LICENSE.txt](https://github.com/open-quantum-safe/testing/blob/master/LICENSE.txt) for details.

Team
----

The Open Quantum Safe project is led by [Douglas Stebila](https://www.douglas.stebila.ca/research/) and [Michele Mosca](http://faculty.iqc.uwaterloo.ca/mmosca/) at the University of Waterloo.

### Contributors

Contributors to this testing repository include:

- Shravan Mishra (University of Waterloo)
- Douglas Stebila (University of Waterloo)

### Support

Financial support for the development of Open Quantum Safe has been provided by Amazon Web Services and the Tutte Institute for Mathematics and Computing.  

We'd like to make a special acknowledgement to the companies who have dedicated programmer time to contribute source code to OQS, including Amazon Web Services, evolutionQ, and Microsoft Research.  

Research projects which developed specific components of OQS have been supported by various research grants, including funding from the Natural Sciences and Engineering Research Council of Canada (NSERC); see the source papers for funding acknowledgments.
