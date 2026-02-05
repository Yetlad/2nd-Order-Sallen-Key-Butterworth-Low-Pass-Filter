

# 2nd-Order Sallen-Key Butterworth Low-Pass Filter

This project details the design, simulation, and verification of a **2nd-order Butterworth low-pass filter** using the **Sallen-Key topology**. The simulation is performed in **LTspice** to analyze the frequency response and verify key filter characteristics.

## 1. Project Objective

To design a filter that attenuates high-frequency noise while maintaining a "maximally flat" response in the passband, with a target cutoff frequency () of approximately **1.1 kHz**.

## 2. Circuit Specifications

* **Topology:** Sallen-Key (Voltage Follower configuration)
* **Filter Type:** Low-pass (Butterworth)
* **Roll-off:** 
* **Components:**
* **Op-Amp:** Powered



## 3. Simulation Parameters (LTspice)

The analysis is conducted using an AC sweep to observe the magnitude response.

* **Source:** `AC Amplitude = 1V`
* **Sweep Type:** Decade (`dec`)
* **Points per Decade:** 200
* **Frequency Range:**  to 
* **Directive:** `.ac dec 200 1 100k`
* **Trace Expression:** `dB(V(vout)/V(vin))`

## 4. Verification Checklist

To confirm the design is successful, the following must be observed in the Bode plot:

1. **Passband Gain:**  (Unity gain).
2. **Cutoff Frequency:** Magnitude should be  at .
3. **Stopband Slope:** A steady decline of  for every tenfold increase in frequency.
4. **Flatness:** No peaks or ripples before the cutoff point.

## 5. Calculations

The theoretical cutoff frequency is calculated as:

Using the provided component values:


---

## 6. Conclusion

The circuit is classified as a **Butterworth filter** because it provides a maximally flat magnitude response in the passband. This is achieved by selecting specific component ratios that result in a quality factor () of , ensuring a smooth transition between the passband and the stopband without gain ripple.

---
