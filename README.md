# firmware/

Pre-compiled OpenClaw firmware binaries.
Source code at: https://github.com/openclaw/openclaw-fw

## Flashing

```bash
# Neural Unit (Arduino Mega 2560 core)
./scripts/flash_neural.sh --port /dev/ttyUSB0 --verify

# PurrSynth (ATtiny84)
./scripts/flash_purrsynth.sh --port /dev/ttyUSB1
```

## Versions

| Binary                         | Target         | Version |
|-------------------------------|----------------|---------|
| openclaw_neural_v0.9.2.bin    | Arduino Mega   | 0.9.2   |
| purrsynth_v2.1.bin            | ATtiny84       | 2.1.0   |

## Serial Protocol (Neural Unit)

```
Frame format: [0xAA][LEN:2BE][CMD:1][PAYLOAD:LEN][CRC8:1]

CMD 0x01  SET_DRIVE
CMD 0x02  GET_DRIVES
CMD 0x10  ENCODE_EVENT
CMD 0x11  GET_TRUST
CMD 0x20  GET_PERSONALITY
CMD 0x21  RESET_PERSONALITY  -- DESTRUCTIVE
CMD 0x30  PING -> PONG
```
