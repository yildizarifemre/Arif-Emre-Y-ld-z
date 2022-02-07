# EMG Signal Acquisition and Data Processing Circuit and Software Development
## Description
The aim of the project is to acquire EMG signals from the human body in real-time and display the contraction times, the amplitude of the contraction. The EMG signals obtained through the electrodes and leads are preprocessed in a circuit that includes an instrumentation amplifier (AD620), a capacitor for linearization, notch filter, active low-pass, and active high-pass filter. After pre-processing, these signals are transmitted to the analog-to-digital converter, which communicates with the computer via the USB cable. In the software, these signals can be monitored in real-time with FFT (Fast Fourier Transform). The software also offers IIR filtering types such as Butterworth, Chebyshev, and elliptic that can be applied to these signals in real-time. Real-time signals can be recorded at the desired time interval for post-processing. The last process involves calculating the contraction times and the contraction amplitude by taking the RMS (Root Mean Square) of the real-time signal.

## Circuit | Development & Design
EMG signals come to the circuit through electrodes and lead. In this application, the three-electrode configuration is used. The circuit is supplied by two 9V batteries. To eliminate artifacts, EMG signals pass through an instrumentation amplifier (AD620) for common-mode rejection and then an active notch filter is applied to eliminate noise at 50 Hz (for Turkey) from the mains voltage, they subsequently pass through an active low-pass filter which is a first-order filter with the cutoff frequency of 40 Hz. Then, they pass through an active high-pass filter which is first-order with the cutoff frequency of 200 Hz.

## Components
•	Electrodes and leads

•	3.5 mm TRS socket

•	AD620 Instrumentation Amplifier

•	LM741 Operational Amplifier

•	Arduino® Uno®

•	USB Cable

•	9V Battery

•	Capacitors and Resistors

## Schematic Design
![image](https://user-images.githubusercontent.com/88987741/152829103-f84fbf6e-252a-45f8-94e8-7c93ac5e846f.png)

## EMG Case Designs
![image](https://user-images.githubusercontent.com/88987741/152828067-c3dff626-5b80-4ed6-8d04-fea4c16387af.png)

## Software | Setup & Capabilities
The software has been developed by using MATLAB's App Designer. The software has been originally developed for Windows OS.

### Real-time Processing, Data Recording and Post Processing

### Capabilities

#### Real-time:

•	EMG monitoring

•	FFT and filtering

•	Monitoring the response of the selected filter

•	Data recording

#### Offline:

•	Loading ECG records with trimming options

•	EMG monitoring

•	Butterworth, Chebyshev, and Elliptic Filtering

•	Ripple option for the selected filter

•	Order option for the selected filter

•	FFT of the selected filter

•	RMS graph

## Disclaimer !!!
Neither the circuit nor the software described above can be used in medical diagnosis or the treatment of any conditions. Otherwise, we cannot be held responsible for any harm or damages.



