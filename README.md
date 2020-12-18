# M202A Project (Formula SAE Datalogger)

This repo contains the report and code for my M202A project. It is important to
clone all of the submodules as well

 - [Project Report](https://rahulsalvi.github.io/M202A_Project/)
 - [Project Presentation](https://www.youtube.com/watch?v=Euvlaq-4Kus&feature=youtu.be)

```bash
$ git clone https://github.com/rahulsalvi/M202A_Project.git
$ cd M202A_Project
$ git submodule update --init --recursive
```

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

## Timeline
 - Week 6: Begin hardware prototype.
 - Week 7: Ability to send and receive CAN messages.
 - Week 8: Serial protocol between Raspberry Pi and MCU working
 - Week 9: Working wireless connectivity and data visualization without delay
   tolerance
 - Week 10: Working delay tolerance system
