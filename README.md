# M202A Project

## Proposal

Motivated by work creating racecars for the Formula SAE student competition, I
want to develop a data logging system that can be used onboard a vehicle. The
system will monitor the vehicle's CANbus and log messages to non-volatile
storage for later consumption. In practice, realtime telemetry is often useful
for quickly diagnosing issues on the racecar. To facilitate this, a host
application running on a ordinary laptop will be created. The application will
establish a wireless connection (either bluetooth or WiFi) to the data logger
to stream and visualize data immediately. During testing, the vehicle passes
through a course much larger than the range of a bluetooth or WiFi network, so
the connection will obviously drop. A form of *delay-tolerant networking* will
be implemented to handle connection issues. The data logger will recognize that
the connection has been dropped and wait until it is re-established. At this
point, it can stream data that was missed back to the host.
