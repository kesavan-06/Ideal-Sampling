# Ideal, Natural, & Flat-top -Sampling
# Aim
Write a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling.

# Program

 import numpy as np
 import matplotlib.pyplot as plt
 from scipy.signal import resample
 fs = 100
 t = np.arange(0, 1, 1/fs) 
 f = 5
 signal = np.sin(2 * np.pi * f * t)
 plt.figure(figsize=(10, 4))
 plt.plot(t, signal, label='Continuous Signal')
 plt.title('Continuous Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show()
 t_sampled = np.arange(0, 1, 1/fs)
 signal_sampled = np.sin(2 * np.pi * f * t_sampled)
 plt.figure(figsize=(10, 4))
 plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
 plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
 plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show()
 reconstructed_signal = resample(signal_sampled, len(t))
 plt.figure(figsize=(10, 4))
 plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
 plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
 plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show() 
# Output Waveform
<img width="1191" height="650" alt="1" src="https://github.com/user-attachments/assets/aa513bbd-06ed-45a1-93ec-71f5cdaf676b" />
<img width="1185" height="704" alt="2" src="https://github.com/user-attachments/assets/738839bb-d2b2-432b-b1b4-5f1c016273af" />
<img width="1104" height="487" alt="3" src="https://github.com/user-attachments/assets/b37e5a59-d124-4682-8b50-72c9e4557e77" />
# Result
Hence a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling.
