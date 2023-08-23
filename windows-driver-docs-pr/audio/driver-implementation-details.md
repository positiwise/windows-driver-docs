---
title: Driver Implementation Details
description: This topic presents the implementation details for an audio driver that is developed for an audio adapter that is capable of processing hardware-offloaded audio streams.
ms.date: 09/30/2022
---

# Driver Implementation Details


This topic presents the implementation details for an audio driver that is developed for an audio adapter that is capable of processing hardware-offloaded audio streams.

In other words, this topic explains what Microsoft has done (starting with Windows 8) to support a driver that works with an audio adapter that is capable of processing hardware-offloaded audio. In the following sections, this topic also shows you what the driver must be capable of to support such an adapter.

## <span id="A__new_Type_GUID_for_node_descriptors"></span><span id="a__new_type_guid_for_node_descriptors"></span><span id="A__NEW_TYPE_GUID_FOR_NODE_DESCRIPTORS"></span>*Type* GUID for node descriptors

If an audio adapter is capable of processing offloaded audio streams, the adapter’s audio driver exposes this capability by using a node in the KS-filter for the adapter.

Each node in the path of the audio stream has a node descriptor, so for this node the driver must set the *Type* GUID to [**KSNODETYPE\_AUDIO\_ENGINE**](./ksnodetype-audio-engine.md). Here’s an example of how the driver could configure the node descriptor for this new node:

```cpp
typedef struct _KSNODE_DESCRIPTOR {
  const KSAUTOMATION_TABLE *AutomationTable;    // drv specific
  const GUID               *Type;       // must be set to KSNODETYPE_AUDIO_ENGINE
  const GUID               *Name;       // drv specific (KSNODETYPE_AUDIO_ENGINE?)  
} KSNODE_DESCRIPTOR, *PKSNODE_DESCRIPTOR;
```

If the Name GUID is set to **KSNODETYPE\_AUDIO\_ENGINE**, then you must create a default name string for this node. You then add that string to *ks.inf*, so that during installation of the driver, the string can be used to populate the *MediaCategories* registry key.

The definition of the GUID for the new node type, **KSNODETYPE\_AUDIO\_ENGINE**, is as follows:

```cpp
Code style
#define STATIC_KSNODETYPE_AUDIO_ENGINE\
    0x35caf6e4, 0xf3b3, 0x4168, 0xbb, 0x4b, 0x55, 0xe7, 0x7a, 0x46, 0x1c, 0x7e
DEFINE_GUIDSTRUCT("35CAF6E4-F3B3-4168-BB4B-55E77A461C7E", KSNODETYPE_AUDIO_ENGINE);
#define KSNODETYPE_AUDIO_ENGINE DEFINE_GUIDNAMED(KSNODETYPE_AUDIO_ENGINE)
```

For more information, see the *ksmedia.h* header file.

And based on the preceding information, a descriptor for a miniport node could look like the following:

```cpp
PCNODE_DESCRIPTOR MiniportNodes[] =
{
    // KSNODE_WAVE_AUDIO_ENGINE
    {
        0,                          // Flags
        NULL,                       // AutomationTable
        &KSNODETYPE_AUDIO_ENGINE,   // Type  KSNODETYPE_AUDIO_ENGINE
        NULL                        // Name
    }
};
```

## <span id="A_new_KS_property_set_for_audio_engines"></span><span id="a_new_ks_property_set_for_audio_engines"></span><span id="A_NEW_KS_PROPERTY_SET_FOR_AUDIO_ENGINES"></span>KS property set for audio engines

Starting with Windows 8, the [KSPROPSETID\_AudioEngine](./kspropsetid-audioengine.md) property set has been introduced to support hardware audio engines and hardware-offloaded audio processing. So the driver for an adapter that can process offloaded audio streams must support the properties in this new property set.

The new property set, **KSPROPSETID\_AudioEngine**, is defined as follows:

```cpp
#define STATIC_KSPROPSETID_AudioEngine\
    0x3A2F82DCL, 0x886F, 0x4BAA, 0x9E, 0xB4, 0x8, 0x2B, 0x90, 0x25, 0xC5, 0x36
DEFINE_GUIDSTRUCT("3A2F82DC-886F-4BAA-9EB4-082B9025C536", KSPROPSETID_AudioEngine);
#define KSPROPSETID_AudioEngine DEFINE_GUIDNAMED(KSPROPSETID_AudioEngine)
```

The names of the properties in this new property set are defined in the [**KSPROPERTY\_AUDIOENGINE**](./ksproperty-audioengine.md) enum, and the driver must support these names.

Here are the new properties in the **KSPROPSETID\_AudioEngine** property set:

[**KSPROPERTY\_AUDIOENGINE\_BUFFER\_SIZE\_RANGE**](./ksproperty-audioengine-buffer-size-limits.md)

[**KSPROPERTY\_AUDIOENGINE\_DESCRIPTOR**](./ksproperty-audioengine-descriptor.md)

[**KSPROPERTY\_AUDIOENGINE\_DEVICEFORMAT**](./ksproperty-audioengine-deviceformat.md)

[**KSPROPERTY\_AUDIOENGINE\_GFXENABLE**](./ksproperty-audioengine-gfx-enable.md)

[**KSPROPERTY\_AUDIOENGINE\_LFXENABLE**](./ksproperty-audioengine-lfx-enable.md)

[**KSPROPERTY\_AUDIOENGINE\_LOOPBACK\_PROTECTION**](./ksproperty-audioengine-loopback-protection.md)

[**KSPROPERTY\_AUDIOENGINE\_MIXFORMAT**](./ksproperty-audioengine-mixformat.md)

[**KSPROPERTY\_AUDIOENGINE\_SUPPORTEDDEVICEFORMATS**](./ksproperty-audioengine-supporteddeviceformats.md)

[**KSPROPERTY\_AUDIOENGINE\_VOLUMELEVEL**](./ksproperty-audioengine-volumelevel.md)

## <span id="Updates_to_the_KSPROPSETID__Audio_property_set"></span><span id="updates_to_the_kspropsetid__audio_property_set"></span><span id="UPDATES_TO_THE_KSPROPSETID__AUDIO_PROPERTY_SET"></span>Updates to the KSPROPSETID\_ Audio property set


In addition to supporting the properties in the **KSPROPSETID\_AudioEngine** property set, the driver must also support the following existing properties in the [KSPROPSETID\_Audio](./kspropsetid-audio.md) property set:

[**KSPROPERTY\_AUDIO\_MUTE**](./ksproperty-audio-mute.md)

[**KSPROPERTY\_AUDIO\_PEAKMETER2**](./ksproperty-audio-peakmeter2.md)

[**KSPROPERTY\_AUDIO\_VOLUMELEVEL**](./ksproperty-audio-volumelevel.md)

And to complete the implementation of driver support for hardware-offloaded audio processing, properties are available to the **KSPROPSETID\_ Audio** property set.

Here are the **KSPROPSETID\_ Audio** properties:

[**KSPROPERTY\_AUDIO\_LINEAR\_BUFFER\_POSITION**](./ksproperty-audio-linear-buffer-position.md)

[**KSPROPERTY\_AUDIO\_PRESENTATION\_POSITION**](./ksproperty-audio-presentation-position.md)

[**KSPROPERTY\_AUDIO\_WAVERT\_CURRENT\_WRITE\_POSITION**](./ksproperty-audio-wavert-current-write-position.md)

## <span id="Port-class_driver_updates_and_glitch_reporting"></span><span id="port-class_driver_updates_and_glitch_reporting"></span><span id="PORT-CLASS_DRIVER_UPDATES_AND_GLITCH_REPORTING"></span>Port-class driver updates and glitch reporting


In addition to the support described in the preceding sections for hardware-offloaded audio processing, the Windows port-class driver has also includes  "helper interfaces" to make it simple to develop a driver that can work with offloaded audio streams. And when such a driver detects glitches, there is a mechanism in place to allow the driver to report the glitch errors. The following topics provide more details about the helper interfaces and glitch reporting:

[Helper Interfaces for Offloaded Audio Processing](helper-interfaces-for-offloaded-audio-processing.md)

[Glitch Reporting for Offloaded Audio](glitch-reporting-for-offloaded-audio.md)

 

