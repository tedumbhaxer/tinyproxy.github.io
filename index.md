# Tinyproxy

Tinyproxy is a light-weight HTTP/HTTPS proxy daemon for POSIX operating systems. Designed from the ground up to be fast and yet small, it is an ideal solution for use cases such as embedded deployments where a full featured HTTP proxy is required, but the system resources for a larger proxy are unavailable.

Tinyproxy is distributed using the GNU GPL license (version 2 or above).

## Features

Tinyproxy has a **small footprint** and requires very little in the way of system resources. The memory footprint tends to be around 2 MB with glibc, and the CPU load increases linearly with the number of simultaneous connections (depending on the speed of the connection). Thus, Tinyproxy can be run on an older machine, or on a network appliance such as a Linux-based broadband router, without any noticeable impact on performance.

Tinyproxy requires only a **minimal POSIX environment** to build and operate. It can use additional libraries to add functionality though.

Tinyproxy allows forwarding of **HTTPS connections** without modifying traffic in any way through the `CONNECT` method (see the `ConnectPort` directive).

Tinyproxy supports being configured as a **transparent proxy**, so that a proxy can be used without requiring any client-side configuration. You can also use it as a **reverse proxy** front-end to your websites.

Using the `AddHeader` directive, you can **add/insert HTTP headers** to outgoing traffic.

If you're looking to build a custom web proxy, Tinyproxy is **easy to modify** to your custom needs. The source is straightforward, adhering to the KISS principle. As such, it can be used as a foundation for anything you may need a web proxy to do.

Tinyproxy has **privacy features** which can let you configure which HTTP headers should be allowed through, and which should be blocked. This allows you to restrict both what data comes to your web browser from the HTTP server (e.g., cookies), and to restrict what data is allowed through from your web browser to the HTTP server (e.g., version information).

Using the **remote monitoring** facility, you can access proxy statistics from afar, letting you know exactly how busy the proxy is.

You can configure Tinyproxy to **control access** by only allowing requests from a certain subnet, or from a certain interface, thus ensuring that random, unauthorized people will not be using your proxy.

With a bit of configuration (specifically, making Tinyproxy created files owned by a non-root user and running it on a port greater than 1024), Tinyproxy can be made to run without any special privileges, thus minimizing the chance of system compromise. Furthermore, it was designed with an eye towards preventing buffer overflows. The simplicity of the code ensures it remains easy to spot such bugs.

## Downloads

* On Red Hat Enterprise Linux, or its derivatives such as CentOS, install Tinyproxy from the EPEL repository by running yum install tinyproxy.
* On Fedora, install Tinyproxy by running yum install tinyproxy.
* On Debian and derived distributions, run apt-get install tinyproxy to install Tinyproxy.
* Arch users can install the Tinyproxy package from the community repository. Run pacman -S tinyproxy to install it.
* FreeBSD, OpenBSD or NetBSD users can use the pkg_add utility to install the tinyproxy package.
* Mac OS X users can check MacPorts to see if the Tinyproxy port there is recent enough.

If you feel that the Tinyproxy binary package in your operating system is not recent, please contact the package maintainer for that particular operating system. If this fails, you can always compile the latest stable version from source code.

We distribute Tinyproxy in source code form, and it has to be compiled in order to be used on your system. Please see the INSTALL file in the source code tree for build instructions. The current stable version of Tinyproxy is available as tinyproxy-1.8.4.tar.bz2. It was released on January 1, 2016. The Tinyproxy 1.8.4 NEWS file contains the release notes. You can verify the tarball using its PGP signature. You can also browse the older releases of Tinyproxy.

We use Git as the version control system for the Tinyproxy source code repository. To get a copy of the Tinyproxy repository, use the command:

git clone https://github.com/tinyproxy/tinyproxy.git

## Documentation

Manpages are the primary documentation for Tinyproxy. After installing Tinyproxy, run the following command to see its manpages:

man tinyproxy tinyproxy.conf

## Support

* Feel free to report a new bug or suggest features via github issues.
* Tinyproxy developers hang out in #tinyproxy on irc.freenode.net.