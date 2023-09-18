# frigate-docker

Configuration for my Frigate installation

## Usage

Create a .env file. Copy `dot.env.example` to `.env` and modify the variables.

Then, run `docker compose up -d`

## Hardware

I'm using a Raspberry Pi 4 with a Coral TPU.

I've also experimented with an Intel Neural Compute Stick 2 (MYRIAD) but don't have a stable configuration for that.

### Intel NCS2 notes

The Neural Compute Stick 2 is a subtype of OpenVINO in Frigate.

It's model configuration isn't compatible with the default model configuration used by the Google Coral boards, and so only one can be active at a time.

Disable the coral, then enable the NCS2 configuration plus it's model section.

https://docs.frigate.video/configuration/detectors#intel-ncs2-vpu-and-myriad-x-setup