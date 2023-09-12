libpsr-container.so:
	rm -rf Container
	mkdir Container
	phptobpc ../src/ContainerExceptionInterface.php > Container/ContainerExceptionInterface.php
	phptobpc ../src/ContainerInterface.php > Container/ContainerInterface.php
	phptobpc ../src/NotFoundExceptionInterface.php > Container/NotFoundExceptionInterface.php
	bpc -v \
		-c bpc.conf  \
		-l psr-container \
		placeholder-container.php \
		Container/ContainerExceptionInterface.php \
		Container/ContainerInterface.php \
		Container/NotFoundExceptionInterface.php

install-libpsr-container:
	bpc -l psr-container --install
