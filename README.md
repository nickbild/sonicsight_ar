# SonicSight AR

![](https://raw.githubusercontent.com/nickbild/visual_alert/main/media/monocle_display_sm.jpg)

Hearing-impaired people face significant challenges due to their inability to perceive auditory cues, such as emergency sirens, alarms, and traffic sounds. These cues are essential for alerting people to potential dangers and ensuring their safety. Without auditory awareness, hearing-impaired people may not be aware of approaching emergency vehicles, fire alarms, or even oncoming traffic, which can lead to life-threatening situations.

According to the World Health Organization, around 466 million people worldwide have disabling hearing loss, which accounts for approximately 5% of the global population. In the United States alone, the Centers for Disease Control and Prevention reported that about 15% of adults aged 18 and over experience some degree of hearing loss.

As an attempt to address this problem, I have created SonicSight AR.  This device uses machine learning to recognize sounds, like emergency vehicles and various types of alarms.  When these sounds are detected, the user of SonicSight AR is alerted to that fact via a message that floats within their visual field through the use of a low-cost augmented reality display.  SonicSight AR also solves some other unique problems often experienced by the hearing-impaired — it also detects footsteps and talking to prevent the wearer from being startled when someone approaches unexpectedly.

## How It Works

The Particle Photon 2 development board is wired to a supported PDM MEMS microphone that comes with the Edge ML Kit for Photon 2.  Wiring schematics can be found in the documentation.  After development is completed, this hardware can be powered by a LiPo battery (a 400 mAh battery was used in this project).

An audio classification neural network was developed with Edge Impulse Studio to distinguish between eight types of sounds (ambulance, danger alarm, fire alarm, firetruck, footsteps, gas alarm, talking, traffic sounds), as well as normal background noises.

When one of the sounds is recognized, the Photon 2 will send a program to a Brilliant Labs Monocle wirelessly via Bluetooth Low Energy, which is attached to a pair of glasses.  This causes text to be overlaid on the wearer’s peripheral vision.  The text provides a visual alert to warn of a sound that otherwise could not be heard.

The Photon 2, microphone, and battery were placed inside a 3D printed case.  A velcro strap was attached to the case such that it could be attached to a belt.

## Media

![](https://raw.githubusercontent.com/nickbild/visual_alert/main/media/all_hw_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/visual_alert/main/media/in_case_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/visual_alert/main/media/case_w_strap_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/visual_alert/main/media/glasses_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/visual_alert/main/media/wearing_sm.jpg)

## Bill of Materials

- 1 x Particle Photon 2
- 1 x PDM MEMS microphone
- 1 x Brilliant Labs Monocle
- 1 x 400 mAh LiPo battery
- optional 3D printed case and lid
- optional velcro strap

## About the Author
[Nick A. Bild, MS](https://nickbild79.firebaseapp.com/#!/)
