# LakeShore 336 Temperature Controller GUI

A Python GUI application for monitoring and controlling the LakeShore 336 Temperature Controller via RS-232 serial interface.  
Developed by Gara Kishor, Research Scholar, Department of Physics, Pondicherry University.

---

## Features

- **RS-232 Serial Communication:** Connects to the LakeShore 336 instrument over serial port.
- **License Key Protection:** Requires an encrypted license key for usage (provided by author).
- **Real-Time Data Acquisition:** Continuously reads and displays temperatures from three sensors (A/B/C).
- **Live Plotting:** Real-time matplotlib plots of temperature vs. time.
- **Heater Control:** Setpoint, ramp, and range (Low/Medium/High/Off) adjustment for two heaters.
- **Data and Plot Export:** Save temperature data as CSV or plot as PDF.
- **Safe Disconnect:** Turns off heaters when disconnecting.
- **User-Friendly Interface:** Built with Tkinter and Matplotlib, easy to use on Windows.

---

## Installation

### Prerequisites

- Python 3.7+
- [PySerial](https://pythonhosted.org/pyserial/)
- [matplotlib](https://matplotlib.org/)
- [tkinter](https://wiki.python.org/moin/TkInter)

Install required packages:

```bash
pip install pyserial matplotlib
```

(Tkinter comes with Python on most distributions.)

---

## Usage

1. **Obtain License Key:**  
   Contact `garakishor6@gmail.com` to request a license key.

2. **Run the Application:**

    ```bash
    python lakeshore_controller.py
    ```

3. **First Run:**  
   You will be prompted to enter your license key. After successful verification, the key is saved for future runs.

4. **Connect to Controller:**
    - Enter your RS-232 COM port (e.g. `COM3`, `COM4`, `/dev/ttyUSB0`).
    - Click **Connect**.

5. **Monitor Temperatures:**
    - Temperatures update every second.
    - Plot displays Sensor A/B/C over time (in minutes).

6. **Heater Controls:**
    - Set heater 1 and 2 setpoints, ramp rates, and ranges.
    - Click **Set Temperatures** and **Set Heater Ranges**.
    - Click **Stop Heaters** to turn heaters off.

7. **Save Data/Plot:**
    - **Save Data** exports all readings to CSV.
    - **Save Plot** exports the current plot as PDF.

8. **Safe Disconnect:**
    - Click **Disconnect** to safely stop the heaters and close the serial port.

---

## File Structure

- `lakeshore_controller.py` — Main application file.
- `license.key` — Generated after successful license entry.
- `TC.ico` — (Optional) Application icon file (for better GUI appearance).

---

## Notes

- The application is intended for experimental/educational use.  
- License is machine/user locked for protection.
- Contact Gara Kishor for feature requests/support.

---

## Credits

**Developed by:**  
Gara Kishor  
Research Scholar, Department of Physics  
Pondicherry University  
Email: garakishor6@gmail.com  
© 2025 Gara Kishor

---

## Troubleshooting

- **"License invalid or expired":** Make sure your key is correct or request a new one.
- **Serial Errors:** Check RS-232 cable, port, and permissions.
- **Plot not updating:** Ensure matplotlib and Tkinter are installed. Try restarting the application.

---

## License

This software is proprietary and protected by license key. Redistribution or modification is not allowed without the author's permission.
