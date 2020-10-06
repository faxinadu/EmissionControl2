# EmissionControl2

EmissionControl2 (EC2) is a new standalone interactive real-time application for granular synthesis and sound file granulation. It is available for OSX, Linux, and Windows. 

![](docs/EC2_lightmode.png "This is what EC2 looks like")

Features include:

- Granulation of multiple sound files simultaneously
- Multiple simultaneous grain streams
- Synchronous and asynchronous grain emission
- Intermittency control
- Per-grain signal processing (envelope, waveform, amplitude, frequency, spatial position, filter center frequency and resonance)
- Unique filter design optimized for per-grain synthesis
- Matrix modulation control of all granulation parameters with six LFOs
- Real-time display of peak amplitude, grain counter, waveform, and scan range
- Scalable GUI and font size
- MIDI Learn enables mapping to any MIDI continuous controller.
- Code is open source and available at GitHub
- Maximal "Grain Integrity" (tm)

See ![releases](https://github.com/jackkilgore/EmissionControl2/releases) page to download the latest version for your operating system.

## Building
### Debian

- This project uses cmake to build so if you don't have cmake then install it (Minimum version: 3.10) and make sure your c and c++ compilers are defined in your environment.

- Run the following in a terminal to install the necessary libraries for building:

`sudo apt install libgtk-3-dev libasound2-dev libsndfile1-dev libfftw3-dev libjack-dev`
 
- git clone the repository 

`git clone https://github.com/jackkilgore/EmissionControl2.git`

- cd into EmissionControl2/ecSource

`cd EmissionControl2/ecSource`

- run configure script:

`./scripts/configure.sh`

- run build script:

`./scripts/build.sh`

- run packaging script:

`./scripts/packageDEB.sh <version>` (you have to provide a version number)

- This should put a .deb file in EmissionControl2/deployment. The deb package is necessary at this stage because it will put all the resources in the correct place on your system.
  
- install the .deb either with your preferred gui app installer or by running: 

`dpkg -i <path-to-the-deb>`


### OS X
You must have cmake installed (version 3.10 or later), and Xcode (hopefully we can get rid of this dependency soon).

- First, clone the repo:

`git clone https://github.com/jackkilgore/EmissionControl2.git`

- cd into EmissionControl2/ecSource

`cd EmissionControl2/ecSource`

- run configure script:

`./scripts/configure.sh`

- run build script:

`./scripts/build.sh`
