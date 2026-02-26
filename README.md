# ruby-companion-cat

```
   |\      _,,,---,,_
   /,`.-'`'    -.  ;-;;,_
  |,4-  ) )-,_..;\ (  `'-'     ruby-companion-cat v0.9.2
 '---''(_/--'  `-'\_)          interactive companion platform
                                powered by openclaw firmware
```

Open-source stack for building an interactive, autonomous companion cat robot.
Ruby is the reference implementation. All hardware is COTS sourced from local
hardware stores, Taobao, or eBay.

## Quickstart

```bash
git clone https://github.com/openclaw/ruby-companion-cat.git
cd ruby-companion-cat
pip install -r requirements.txt
./scripts/flash_neural.sh --port /dev/ttyUSB0 --verify
./scripts/flash_purrsynth.sh --port /dev/ttyUSB1
python3 scripts/calibrate_sensefur.py --output config/sensefur_cal.bin
python3 -m ruby.runtime --config config.yaml
```

See full docs in each module directory.

## License

MIT License. Copyright (c) 2025 OpenClaw Contributors.
