# Indoor localization using RSSI information in challenging environments

## Motivation

## Background

Indoor localization or indoor positioning systems are systems with the ability to locate objects or people inside a building using radio waves, magnetic fields, acoustic signals, or other sensory information collected by mobile devices. Those systems are an integral part of many applications location-based applications and services including: environmental monitoring, civil services, military purposes, etc.
<p align="center">
<img src="https://cloud.githubusercontent.com/assets/7999611/22739126/8e0b5d1e-ee0a-11e6-92b9-bcaa66138680.png">
</p>
Traditional localization systems like the most popular satellite based Global Positioning System (GPS) are adequate for localizing objects in outdoor environments
(typical applications are tracking and asset management, transport navigation and guidance, synchronization of telecommunications networks, etc.
However, the signal from the GPS satellites is too weak to come across most buildings thus making GPS ineffective for indoor localization.


## Indoor localization systems and challenges

Indoor localization solutions address the inadequacy of global positioning system to provide precise object position inside a closed (indoor) environment
(e.g. a shopping mall, hospitals, airport, a subway, and university campuses, etc.).
By the complex nature of indoor environments, the development of an indoor localization technique is always associated with a set of challenges like smaller dimensions,
high none line of sight (NLOS), influence of obstacles like walls, equipment, movement of human beings, doors, and other factors. 
Multipath effect signals are reflected and attenuated by walls and furniture and noise interference. These challenges result mainly from the influence of obstacles on the propagation of electromagnetic waves. For getting good and accurate results, a positioning system must be able to handle these problems [1].

An indoor localization system typically consists of 3 elements: 
* A wireless (mobile) object that has to be localized, also called the mobile station (MS);
* A set of fixed wireless devices that send or collect sensory measurements to/from the target device (called anchor points, AP);
* A localization algorithm which is the heart of the overall system in charge of estimating the target's position based on the measurements obtained from the APs.

<p align="center">
<img src="https://cloud.githubusercontent.com/assets/7999611/22739780/786c59a6-ee0d-11e6-9b7d-ade84f5b1d5d.png">
</p>

**Wireless technologies used for indoor localization.**
The most prominent state-of-the-art wireless technologies and devices used for disseminating indoor positioning systems are:
- Infrared radiation (IR)
- Radio frequency identification (RFID)
- Ultrawideband (UWB)
- Bluetooth
- Wireless LAN (WiFi)
- Zigbee

Those technologies typically differ in range and the localization accuracy (the difference between the real position of the MS and the position estimated by the localization algorithm) that can be achieved using them for wireless communication.
For more details please take a look at [1] and [2].


## Indoor localization approaches

The localization algorithm is the heart and the intelligent part of an indoor localization system.
It can be deployed at the MS device itself or at a backend server. With regard to this, there are two
architectural implementations of localization systems:
* Server-based. Information is obtain from the MS and forwarded to a backend system as input for the localization algorithm that estimates the position of the MS.
* Mobile station-based. The MS uses information from the APs in order to estimate its position.

<p align="center">
<img src="https://cloud.githubusercontent.com/assets/7999611/22739998/65ab4420-ee0e-11e6-91bf-8d4f871ebb80.png">
</p>


Depending on the type of the localization algorithm there are several indoor localization approaches. They typically fall into one of the following categories:
*  **Fingerprinting**. Fingerprinting consists of two phases:
  1. Scene analysis or site survey. This is the offline training phase when measurements are collected from the environment at known locations (i.e. reference points, RP) called fingerprints to build a fingerprinting database or radio map. Basically, a radio map is a database of spots at predefined points (coordinates)
coupled with various radio signal characteristics, for example, signal angles, or propagation time called signal
fingerprints.
  2. Localization phase. This is the online phase when the location of the object is
determined by matching/comparing online measurements at unknown locations with the ones from the radio map and the
closest match location is selected.

*  **Range-based**. Range-based localization approaches consist of two phases:
  1. Estimating the distance or the angle towards several APs. This can be done using different types of measurements/information, such as: RSSI (Received Signal Strength Indicator), ToA (Time of Arrival), TDoA (Time Difference of Arrival), AoA (Angle of Arrival), etc.
  2. Localization phase- Using the estimated distances as input to a localization algorithm to determinge the position 
of the MS node. Examples are: Maximum likelihood, multilateration, triangualtion, Bounding-Box, etc.

*  **Proximity**. This is the simplest approach also called connectivity based positioning, where the location of the object is determined based on cell of origin (CoO), e.g. GSM-ID. It provides only symbolic relative location information.

<p align="center">
<img src="https://cloud.githubusercontent.com/assets/7999611/22740527/805725bc-ee10-11e6-81b9-71bc920b0552.png">
</p>





