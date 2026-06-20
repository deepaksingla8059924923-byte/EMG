## System Architecture

```text
Electrodes
    │
    ▼
 ADS1299
    │
    ▼
 ESP32-S3
  ├── USB ───► Computer (ML)
  └── microSD (Logging)
```
```

### Data Flow

1. Electrodes acquire EEG and EMG signals.
2. ADS1299 digitizes the signals at 24-bit resolution.
3. ESP32-S3 receives data via SPI.
4. Data is:
   - Sent to a computer over USB for machine learning.
   - Logged to a microSD card for backup.

> **Note:** USB is the primary interface for data collection and ML training.
