npipe
=====

A Windows named pipe implementation written in pure Go.

See documentation at http://godoc.org/github.com/natefinch/npipe

Written for Go 1.1.

What's Missing
--------------

Timeouts for the connections are currently not implemented.


How to Build
============

The z files contain new syscalls that don't exist in the standard library.

They are generated by running

$gosource/src/pkg/syscall/mksyscall_windows.pl npipe_windows.go > znpipe_windows.go
$gosource/src/pkg/syscall/mksyscall_windows.pl -l32 npipe_windows.go > znpipe_windows.go

Otherwise it's a normal Go package.

