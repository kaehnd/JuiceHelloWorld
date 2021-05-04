# Automatically generated makefile, created by the Projucer
# Don't edit this file! Your changes will be overwritten when you re-save the Projucer project!

cmake_minimum_required(VERSION 3.4.1)

set(BINARY_NAME "juce_jni")

set(OBOE_DIR "C:/Program Files/JUCE/modules/juce_audio_devices/native/oboe")

add_subdirectory (${OBOE_DIR} ./oboe)

add_library("cpufeatures" STATIC "${ANDROID_NDK}/sources/android/cpufeatures/cpu-features.c")
set_source_files_properties("${ANDROID_NDK}/sources/android/cpufeatures/cpu-features.c" PROPERTIES COMPILE_FLAGS "-Wno-sign-conversion -Wno-gnu-statement-expression")

add_definitions("-DJUCE_ANDROID=1" "-DJUCE_ANDROID_API_VERSION=16" "-DJUCE_PUSH_NOTIFICATIONS=1" "-DJUCE_PUSH_NOTIFICATIONS_ACTIVITY=\"com/rmsl/juce/JuceActivity\"" "-DPIP_JUCE_EXAMPLES_DIRECTORY=QzpcUHJvZ3JhbSBGaWxlc1xKVUNFXGV4YW1wbGVz" "-DJUCER_ANDROIDSTUDIO_7F0E4A25=1" "-DJUCE_APP_VERSION=1.0.0" "-DJUCE_APP_VERSION_HEX=0x10000")

include_directories( AFTER
    "../../../JuceLibraryCode"
    "C:/Program Files/JUCE/modules"
    "${ANDROID_NDK}/sources/android/cpufeatures"
)

enable_language(ASM)

if(JUCE_BUILD_CONFIGURATION MATCHES "DEBUG")
    add_definitions("-DJUCE_DISPLAY_SPLASH_SCREEN=1" "-DJUCE_USE_DARK_SPLASH_SCREEN=1" "-DJUCE_PROJUCER_VERSION=0x60008" "-DJUCE_MODULE_AVAILABLE_juce_audio_basics=1" "-DJUCE_MODULE_AVAILABLE_juce_audio_devices=1" "-DJUCE_MODULE_AVAILABLE_juce_audio_formats=1" "-DJUCE_MODULE_AVAILABLE_juce_audio_processors=1" "-DJUCE_MODULE_AVAILABLE_juce_audio_utils=1" "-DJUCE_MODULE_AVAILABLE_juce_core=1" "-DJUCE_MODULE_AVAILABLE_juce_data_structures=1" "-DJUCE_MODULE_AVAILABLE_juce_events=1" "-DJUCE_MODULE_AVAILABLE_juce_graphics=1" "-DJUCE_MODULE_AVAILABLE_juce_gui_basics=1" "-DJUCE_MODULE_AVAILABLE_juce_gui_extra=1" "-DJUCE_GLOBAL_MODULE_SETTINGS_INCLUDED=1" "-DJUCE_STRICT_REFCOUNTEDPOINTER=1" "-DJUCE_STANDALONE_APPLICATION=1" "-DPIP_JUCE_EXAMPLES_DIRECTORY=QzpcUHJvZ3JhbSBGaWxlc1xKVUNFXGV4YW1wbGVz" "-DJUCER_ANDROIDSTUDIO_7F0E4A25=1" "-DJUCE_APP_VERSION=1.0.0" "-DJUCE_APP_VERSION_HEX=0x10000" "-DDEBUG=1" "-D_DEBUG=1")
elseif(JUCE_BUILD_CONFIGURATION MATCHES "RELEASE")
    add_definitions("-DJUCE_DISPLAY_SPLASH_SCREEN=1" "-DJUCE_USE_DARK_SPLASH_SCREEN=1" "-DJUCE_PROJUCER_VERSION=0x60008" "-DJUCE_MODULE_AVAILABLE_juce_audio_basics=1" "-DJUCE_MODULE_AVAILABLE_juce_audio_devices=1" "-DJUCE_MODULE_AVAILABLE_juce_audio_formats=1" "-DJUCE_MODULE_AVAILABLE_juce_audio_processors=1" "-DJUCE_MODULE_AVAILABLE_juce_audio_utils=1" "-DJUCE_MODULE_AVAILABLE_juce_core=1" "-DJUCE_MODULE_AVAILABLE_juce_data_structures=1" "-DJUCE_MODULE_AVAILABLE_juce_events=1" "-DJUCE_MODULE_AVAILABLE_juce_graphics=1" "-DJUCE_MODULE_AVAILABLE_juce_gui_basics=1" "-DJUCE_MODULE_AVAILABLE_juce_gui_extra=1" "-DJUCE_GLOBAL_MODULE_SETTINGS_INCLUDED=1" "-DJUCE_STRICT_REFCOUNTEDPOINTER=1" "-DJUCE_STANDALONE_APPLICATION=1" "-DPIP_JUCE_EXAMPLES_DIRECTORY=QzpcUHJvZ3JhbSBGaWxlc1xKVUNFXGV4YW1wbGVz" "-DJUCER_ANDROIDSTUDIO_7F0E4A25=1" "-DJUCE_APP_VERSION=1.0.0" "-DJUCE_APP_VERSION_HEX=0x10000" "-DNDEBUG=1")
else()
    message( FATAL_ERROR "No matching build-configuration found." )
endif()

add_library( ${BINARY_NAME}

    SHARED

    "../../../Source/Main.cpp"
    "../../../Source/AudioSynthesiserDemo.h"
    "../../../Source/DemoUtilities.h"
    "../../../Source/AudioLiveScrollingDisplay.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/audio_play_head/juce_AudioPlayHead.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioChannelSet.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioChannelSet.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioDataConverters.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioDataConverters.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioProcessLoadMeasurer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioProcessLoadMeasurer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioSampleBuffer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_FloatVectorOperations.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_FloatVectorOperations.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiBuffer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiBuffer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiFile.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiFile.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiKeyboardState.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiKeyboardState.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiMessage.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiMessage.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiMessageSequence.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiMessageSequence.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiRPN.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiRPN.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEInstrument.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEInstrument.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEMessages.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEMessages.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPENote.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPENote.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiserBase.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiserBase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiserVoice.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiserVoice.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEUtils.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEUtils.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEValue.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEValue.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEZoneLayout.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEZoneLayout.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/native/juce_mac_CoreAudioLayouts.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_AudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_BufferingAudioSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_BufferingAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ChannelRemappingAudioSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ChannelRemappingAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_IIRFilterAudioSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_IIRFilterAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_MemoryAudioSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_MemoryAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_MixerAudioSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_MixerAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_PositionableAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ResamplingAudioSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ResamplingAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ReverbAudioSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ReverbAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ToneGeneratorAudioSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ToneGeneratorAudioSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/synthesisers/juce_Synthesiser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/synthesisers/juce_Synthesiser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_ADSR.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_ADSR_test.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_Decibels.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_GenericInterpolator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_IIRFilter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_IIRFilter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_Interpolators.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_Interpolators.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_LagrangeInterpolator.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_Reverb.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_SmoothedValue.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_SmoothedValue.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_WindowedSincInterpolator.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/juce_audio_basics.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/juce_audio_basics.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/juce_audio_basics.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioDeviceManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioDeviceManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioIODevice.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioIODevice.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioIODeviceType.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioIODeviceType.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_SystemAudioVolume.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPacket.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPackets.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPBytestreamInputHandler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPConversion.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPConverters.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPDispatcher.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPFactory.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPIterator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPMidi1ToBytestreamTranslator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPMidi1ToMidi2DefaultTranslator.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPMidi1ToMidi2DefaultTranslator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPProtocols.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPReceiver.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPSysEx7.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPSysEx7.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPTests.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPU32InputHandler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPUtils.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPUtils.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPView.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPView.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/juce_MidiDevices.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/juce_MidiDevices.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/juce_MidiMessageCollector.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/juce_MidiMessageCollector.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/AudioStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/AudioStreamBase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/AudioStreamBuilder.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/AudioStreamCallback.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/Definitions.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/LatencyTuner.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/Oboe.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/ResultWithValue.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/StabilizedCallback.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/Utilities.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/Version.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AAudioExtensions.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AAudioLoader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AAudioLoader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AudioStreamAAudio.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AudioStreamAAudio.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioClock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioSourceCaller.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioSourceCaller.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioStreamBuilder.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/DataConversionFlowGraph.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/DataConversionFlowGraph.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FilterAudioStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FilterAudioStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockAdapter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockAdapter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockReader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockReader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockWriter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockWriter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/LatencyTuner.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/MonotonicCounter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/OboeDebug.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/QuirksManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/QuirksManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/SourceFloatCaller.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/SourceFloatCaller.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/SourceI16Caller.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/SourceI16Caller.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/StabilizedCallback.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/Trace.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/Trace.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/Utilities.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/Version.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoBuffer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoBuffer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoController.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoController.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoControllerBase.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoControllerBase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoControllerIndirect.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoControllerIndirect.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/HyperbolicCosineWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/IntegerRatio.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/IntegerRatio.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/KaiserWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/LinearResampler.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/LinearResampler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/MultiChannelResampler.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/MultiChannelResampler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResampler.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResampler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResamplerMono.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResamplerMono.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResamplerStereo.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResamplerStereo.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/SincResampler.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/SincResampler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/SincResamplerStereo.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/SincResamplerStereo.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ChannelCountConverter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ChannelCountConverter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ClipToRange.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ClipToRange.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/FlowGraphNode.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/FlowGraphNode.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ManyToMultiConverter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ManyToMultiConverter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/MonoToMultiConverter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/MonoToMultiConverter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/MultiToMonoConverter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/MultiToMonoConverter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/RampLinear.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/RampLinear.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SampleRateConverter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SampleRateConverter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkFloat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkFloat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkI16.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkI16.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkI24.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkI24.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceFloat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceFloat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceI16.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceI16.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceI24.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceI24.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioInputStreamOpenSLES.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioInputStreamOpenSLES.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioOutputStreamOpenSLES.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioOutputStreamOpenSLES.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioStreamBuffered.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioStreamBuffered.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioStreamOpenSLES.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioStreamOpenSLES.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/EngineOpenSLES.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/EngineOpenSLES.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/OpenSLESUtilities.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/OpenSLESUtilities.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/OutputMixerOpenSLES.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/OutputMixerOpenSLES.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/CMakeLists.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/readme.md"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_Audio.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_HighPerformanceAudioHelpers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_Midi.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_Oboe.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_OpenSL.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_ios_Audio.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_ios_Audio.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_linux_ALSA.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_linux_Bela.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_linux_JackAudio.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_linux_Midi.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_mac_CoreAudio.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_mac_CoreMidi.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_MidiDataConcatenator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_win32_ASIO.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_win32_DirectSound.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_win32_Midi.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_win32_WASAPI.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/sources/juce_AudioSourcePlayer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/sources/juce_AudioSourcePlayer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/sources/juce_AudioTransportSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/sources/juce_AudioTransportSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/juce_audio_devices.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/juce_audio_devices.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/juce_audio_devices.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/all.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/bitmath.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/bitreader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/bitwriter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/cpu.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/crc.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/fixed.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/float.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/format.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/lpc.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/md5.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/memory.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/metadata.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/stream_encoder.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/stream_encoder_framing.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/window.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/protected/all.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/protected/stream_decoder.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/protected/stream_encoder.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/bitmath.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/bitreader.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/bitwriter.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/cpu.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/crc.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/fixed.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/float.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/format.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/lpc_flac.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/md5.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/memory.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/stream_decoder.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/stream_encoder.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/stream_encoder_framing.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/window_flac.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/all.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/alloc.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/assert.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/callback.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/compat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/endswap.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/export.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/Flac Licence.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/format.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/metadata.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/ordinals.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/stream_decoder.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/stream_encoder.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/win_utf8_io.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/books/coupled/res_books_51.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/books/coupled/res_books_stereo.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/books/floor/floor_books.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/books/uncoupled/res_books_uncoupled.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/floor_all.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/psych_8.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/psych_11.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/psych_16.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/psych_44.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_8.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_16.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_44.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_44p51.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_44u.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_8.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_11.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_16.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_22.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_32.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_44.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_44p51.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_44u.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_X.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/analysis.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/backends.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/bitrate.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/bitrate.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/block.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/codebook.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/codebook.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/codec_internal.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/envelope.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/envelope.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/floor0.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/floor1.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/highlevel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/info.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lookup.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lookup.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lookup_data.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lpc.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lpc.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lsp.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lsp.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/mapping0.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/masking.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/mdct.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/mdct.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/misc.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/misc.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/os.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/psy.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/psy.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/registry.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/registry.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/res0.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/scales.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/sharedbook.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/smallft.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/smallft.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/synthesis.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/vorbisenc.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/vorbisfile.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/window.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/window.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/README.md"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/bitwise.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/codec.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/config_types.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/crctable.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/framing.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/Ogg Vorbis Licence.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/ogg.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/os_types.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/vorbisenc.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/vorbisfile.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_AiffAudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_AiffAudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_CoreAudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_CoreAudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_FlacAudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_FlacAudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_LAMEEncoderAudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_LAMEEncoderAudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_MP3AudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_MP3AudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_OggVorbisAudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_OggVorbisAudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_WavAudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_WavAudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_WindowsMediaAudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_WindowsMediaAudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatReader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatReader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatReaderSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatReaderSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatWriter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatWriter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioSubsectionReader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioSubsectionReader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_BufferingAudioFormatReader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_BufferingAudioFormatReader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_MemoryMappedAudioFormatReader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/sampler/juce_Sampler.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/sampler/juce_Sampler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/juce_audio_formats.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/juce_audio_formats.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/juce_audio_formats.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format/juce_AudioPluginFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format/juce_AudioPluginFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format/juce_AudioPluginFormatManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format/juce_AudioPluginFormatManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/baseiids.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/classfactoryhelpers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fbuffer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fbuffer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fdebug.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fdebug.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fobject.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fobject.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fstreamer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fstreamer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fstring.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fstring.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/updatehandler.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/updatehandler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/thread/include/flock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/thread/source/flock.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/LICENSE.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/README.md"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/conststringtable.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/conststringtable.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/coreiids.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/falignpop.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/falignpush.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/fplatform.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/fstrdefs.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ftypes.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/funknown.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/funknown.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/futils.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/fvariant.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ibstream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/icloneable.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ipersistent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ipluginbase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/istringresult.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/iupdatehandler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/smartpointer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/typesizecheck.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ustring.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ustring.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/gui/iplugview.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/gui/iplugviewcontentscalesupport.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstattributes.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstaudioprocessor.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstautomationstate.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstchannelcontextinfo.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstcomponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstcontextmenu.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivsteditcontroller.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstevents.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivsthostapplication.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstinterappaudio.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstmessage.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstmidicontrollers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstmidilearn.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstnoteexpression.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstparameterchanges.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstphysicalui.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstpluginterfacesupport.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstplugview.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstprefetchablesupport.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstprocesscontext.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstrepresentation.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivsttestplugprovider.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstunits.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/vstpshpack4.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/vstspeaker.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/vsttypes.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/LICENSE.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/README.md"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/common/memorystream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/common/memorystream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/common/pluginview.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/common/pluginview.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/hosting/hostclasses.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/hosting/hostclasses.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/hosting/pluginterfacesupport.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/hosting/pluginterfacesupport.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstbus.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstbus.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstcomponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstcomponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstcomponentbase.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstcomponentbase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vsteditcontroller.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vsteditcontroller.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstinitiids.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstparameters.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstparameters.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstpresetfile.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstpresetfile.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/LICENSE.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/README.md"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/JUCE_README.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/LICENSE.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/README.md"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_AU_Shared.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_AudioUnitPluginFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_AudioUnitPluginFormat.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_LADSPAPluginFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_LADSPAPluginFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_LegacyAudioParameter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VST3Common.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VST3Headers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VST3PluginFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VST3PluginFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VSTCommon.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VSTMidiEventList.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VSTPluginFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VSTPluginFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioPluginInstance.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioPluginInstance.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessor.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessor.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorEditor.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorEditor.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorGraph.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorGraph.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorListener.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorParameter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorParameterGroup.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorParameterGroup.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_GenericAudioProcessorEditor.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_GenericAudioProcessorEditor.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_PluginDescription.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_PluginDescription.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_KnownPluginList.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_KnownPluginList.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_PluginDirectoryScanner.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_PluginDirectoryScanner.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_PluginListComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_PluginListComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterBool.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterBool.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterChoice.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterChoice.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterFloat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterFloat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterInt.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterInt.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioProcessorParameterWithID.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioProcessorParameterWithID.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioProcessorValueTreeState.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioProcessorValueTreeState.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_ParameterAttachments.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_ParameterAttachments.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_PluginHostType.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_PluginHostType.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_RangedAudioParameter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_RangedAudioParameter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/juce_audio_processors.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/juce_audio_processors.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/juce_audio_processors.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/audio_cd/juce_AudioCDBurner.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/audio_cd/juce_AudioCDReader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/audio_cd/juce_AudioCDReader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioAppComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioAppComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioDeviceSelectorComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioDeviceSelectorComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnail.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnail.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnailBase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnailCache.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnailCache.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioVisualiserComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioVisualiserComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_BluetoothMidiDevicePairingDialogue.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_MidiKeyboardComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_MidiKeyboardComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_android_BluetoothMidiDevicePairingDialogue.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_ios_BluetoothMidiDevicePairingDialogue.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_linux_AudioCDReader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_linux_BluetoothMidiDevicePairingDialogue.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_mac_AudioCDBurner.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_mac_AudioCDReader.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_mac_BluetoothMidiDevicePairingDialogue.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_win_BluetoothMidiDevicePairingDialogue.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_win32_AudioCDBurner.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_win32_AudioCDReader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/players/juce_AudioProcessorPlayer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/players/juce_AudioProcessorPlayer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/players/juce_SoundPlayer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/players/juce_SoundPlayer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/juce_audio_utils.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/juce_audio_utils.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/juce_audio_utils.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_AbstractFifo.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_AbstractFifo.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_Array.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ArrayAllocationBase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ArrayBase.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ArrayBase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_DynamicObject.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_DynamicObject.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ElementComparator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_HashMap.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_HashMap_test.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_LinkedListPointer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ListenerList.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_NamedValueSet.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_NamedValueSet.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_OwnedArray.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_OwnedArray.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_PropertySet.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_PropertySet.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ReferenceCountedArray.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ReferenceCountedArray.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ScopedValueSetter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_SortedSet.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_SparseSet.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_SparseSet.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_Variant.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_Variant.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_DirectoryIterator.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_DirectoryIterator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_File.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_File.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileFilter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileFilter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileInputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileInputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileOutputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileOutputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileSearchPath.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileSearchPath.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_MemoryMappedFile.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_RangedDirectoryIterator.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_RangedDirectoryIterator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_TemporaryFile.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_TemporaryFile.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_WildcardFileFilter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_WildcardFileFilter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/javascript/juce_Javascript.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/javascript/juce_Javascript.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/javascript/juce_JSON.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/javascript/juce_JSON.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/logging/juce_FileLogger.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/logging/juce_FileLogger.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/logging/juce_Logger.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/logging/juce_Logger.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_BigInteger.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_BigInteger.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Expression.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Expression.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_MathsFunctions.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_NormalisableRange.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Random.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Random.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Range.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_StatisticsAccumulator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_AllocationHooks.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_AllocationHooks.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_Atomic.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_ByteOrder.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_ContainerDeletePolicy.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_HeapBlock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_HeavyweightLeakedObjectDetector.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_LeakedObjectDetector.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_Memory.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_MemoryBlock.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_MemoryBlock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_OptionalScopedPointer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_ReferenceCountedObject.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_ScopedPointer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_SharedResourcePointer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_Singleton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_WeakReference.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_ConsoleApplication.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_ConsoleApplication.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_Result.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_Result.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_RuntimePermissions.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_RuntimePermissions.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_Uuid.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_Uuid.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_WindowsRegistry.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/java/README.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_Files.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_JNIHelpers.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_JNIHelpers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_Misc.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_Network.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_RuntimePermissions.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_SystemStats.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_Threads.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_BasicNativeHeaders.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_curl_Network.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_intel_SharedCode.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_CommonFile.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_Files.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_Network.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_SystemStats.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_Threads.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_CFHelpers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_ClangBugWorkaround.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_Files.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_Network.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_ObjCHelpers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_Strings.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_SystemStats.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_Threads.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_posix_IPAddress.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_posix_NamedPipe.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_posix_SharedCode.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_wasm_SystemStats.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_ComSmartPtr.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_Files.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_Network.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_Registry.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_SystemStats.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_Threads.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_IPAddress.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_IPAddress.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_MACAddress.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_MACAddress.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_NamedPipe.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_NamedPipe.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_Socket.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_Socket.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_URL.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_URL.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_WebInputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_WebInputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_BufferedInputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_BufferedInputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_FileInputSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_FileInputSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_InputSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_InputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_InputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_MemoryInputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_MemoryInputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_MemoryOutputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_MemoryOutputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_OutputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_OutputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_SubregionStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_SubregionStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_URLInputSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_URLInputSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_CompilerSupport.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_CompilerWarnings.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_PlatformDefs.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_StandardHeader.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_SystemStats.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_SystemStats.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_TargetPlatform.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_Base64.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_Base64.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharacterFunctions.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharacterFunctions.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharPointer_ASCII.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharPointer_UTF8.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharPointer_UTF16.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharPointer_UTF32.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_Identifier.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_Identifier.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_LocalisedStrings.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_LocalisedStrings.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_NewLine.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_String.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_String.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringArray.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringArray.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringPairArray.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringPairArray.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringPool.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringPool.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringRef.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_TextDiff.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_TextDiff.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ChildProcess.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ChildProcess.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_CriticalSection.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_DynamicLibrary.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_HighResolutionTimer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_HighResolutionTimer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_InterProcessLock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_Process.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ReadWriteLock.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ReadWriteLock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ScopedLock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ScopedReadLock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ScopedWriteLock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_SpinLock.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_Thread.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_Thread.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ThreadLocalValue.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ThreadPool.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ThreadPool.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_TimeSliceThread.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_TimeSliceThread.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_WaitableEvent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_WaitableEvent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_PerformanceCounter.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_PerformanceCounter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_RelativeTime.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_RelativeTime.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_Time.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_Time.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/unit_tests/juce_UnitTest.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/unit_tests/juce_UnitTest.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/unit_tests/juce_UnitTestCategories.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/xml/juce_XmlDocument.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/xml/juce_XmlDocument.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/xml/juce_XmlElement.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/xml/juce_XmlElement.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/adler32.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/compress.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/crc32.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/crc32.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/deflate.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/deflate.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/infback.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inffast.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inffast.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inffixed.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inflate.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inflate.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inftrees.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inftrees.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/trees.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/trees.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/uncompr.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zconf.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zconf.in.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zlib.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zutil.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zutil.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_GZIPCompressorOutputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_GZIPCompressorOutputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_GZIPDecompressorInputStream.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_GZIPDecompressorInputStream.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_ZipFile.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_ZipFile.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/juce_core.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/juce_core.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_core/juce_core.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/app_properties/juce_ApplicationProperties.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/app_properties/juce_ApplicationProperties.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/app_properties/juce_PropertiesFile.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/app_properties/juce_PropertiesFile.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/undomanager/juce_UndoableAction.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/undomanager/juce_UndoManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/undomanager/juce_UndoManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_CachedValue.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_CachedValue.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_Value.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_Value.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueTree.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueTree.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueTreeSynchroniser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueTreeSynchroniser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueWithDefault.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueWithDefault.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/juce_data_structures.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/juce_data_structures.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/juce_data_structures.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ActionBroadcaster.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ActionBroadcaster.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ActionListener.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_AsyncUpdater.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_AsyncUpdater.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ChangeBroadcaster.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ChangeBroadcaster.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ChangeListener.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_ConnectedChildProcess.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_ConnectedChildProcess.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_InterprocessConnection.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_InterprocessConnection.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_InterprocessConnectionServer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_InterprocessConnectionServer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_NetworkServiceDiscovery.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_NetworkServiceDiscovery.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_ApplicationBase.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_ApplicationBase.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_CallbackMessage.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_DeletedAtShutdown.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_DeletedAtShutdown.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_Initialisation.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_Message.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MessageListener.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MessageListener.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MessageManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MessageManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MountedVolumeListChangeDetector.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_NotificationType.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_android_Messaging.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_ios_MessageManager.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_linux_EventLoop.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_linux_Messaging.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_mac_MessageManager.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_osx_MessageQueue.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_win32_HiddenMessageWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_win32_Messaging.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_win32_WinRTWrapper.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_win32_WinRTWrapper.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/timers/juce_MultiTimer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/timers/juce_MultiTimer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/timers/juce_Timer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/timers/juce_Timer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/juce_events.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/juce_events.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_events/juce_events.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_Colour.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_Colour.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_ColourGradient.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_ColourGradient.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_Colours.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_Colours.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_FillType.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_FillType.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_PixelFormats.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_GraphicsContext.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_GraphicsContext.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsContext.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsPostScriptRenderer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsPostScriptRenderer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsSoftwareRenderer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsSoftwareRenderer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_DropShadowEffect.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_DropShadowEffect.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_GlowEffect.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_GlowEffect.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_ImageEffectFilter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_AttributedString.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_AttributedString.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_CustomTypeface.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_CustomTypeface.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_Font.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_Font.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_GlyphArrangement.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_GlyphArrangement.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_TextLayout.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_TextLayout.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_Typeface.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_Typeface.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_AffineTransform.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_AffineTransform.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_BorderSize.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_EdgeTable.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_EdgeTable.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Line.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Parallelogram.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Path.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Path.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_PathIterator.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_PathIterator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_PathStrokeType.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_PathStrokeType.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Point.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Rectangle.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_RectangleList.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/cderror.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/changes to libjpeg for JUCE.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcapimin.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcapistd.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jccoefct.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jccolor.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcdctmgr.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jchuff.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jchuff.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcinit.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcmainct.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcmarker.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcmaster.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcomapi.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jconfig.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcparam.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcphuff.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcprepct.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcsample.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jctrans.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdapimin.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdapistd.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdatasrc.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdcoefct.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdcolor.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdct.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jddctmgr.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdhuff.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdhuff.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdinput.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdmainct.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdmarker.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdmaster.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdmerge.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdphuff.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdpostct.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdsample.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdtrans.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jerror.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jerror.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jfdctflt.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jfdctfst.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jfdctint.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jidctflt.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jidctfst.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jidctint.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jidctred.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jinclude.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jmemmgr.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jmemnobs.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jmemsys.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jmorecfg.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jpegint.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jpeglib.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jquant1.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jquant2.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jutils.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jversion.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/transupp.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/transupp.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/libpng_readme.txt"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/png.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/png.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngconf.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngdebug.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngerror.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngget.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pnginfo.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngmem.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngpread.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngpriv.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngread.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngrio.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngrtran.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngrutil.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngset.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngstruct.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngtrans.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngwio.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngwrite.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngwtran.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngwutil.c"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/juce_GIFLoader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/juce_JPEGLoader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/juce_PNGLoader.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_Image.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_Image.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageCache.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageCache.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageConvolutionKernel.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageConvolutionKernel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageFileFormat.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageFileFormat.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_android_Fonts.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_android_GraphicsContext.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_android_IconHelpers.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_freetype_Fonts.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_linux_Fonts.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_linux_IconHelpers.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_CoreGraphicsContext.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_CoreGraphicsContext.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_CoreGraphicsHelpers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_Fonts.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_IconHelpers.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_RenderingHelpers.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_Direct2DGraphicsContext.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_Direct2DGraphicsContext.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_DirectWriteTypeface.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_DirectWriteTypeLayout.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_Fonts.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_IconHelpers.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/placement/juce_Justification.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/placement/juce_RectanglePlacement.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/placement/juce_RectanglePlacement.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/juce_graphics.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/juce_graphics.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/juce_graphics.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/application/juce_Application.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/application/juce_Application.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ArrowButton.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ArrowButton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_Button.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_Button.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_DrawableButton.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_DrawableButton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_HyperlinkButton.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_HyperlinkButton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ImageButton.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ImageButton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ShapeButton.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ShapeButton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_TextButton.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_TextButton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ToggleButton.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ToggleButton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ToolbarButton.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ToolbarButton.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandID.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandInfo.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandInfo.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandTarget.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandTarget.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_KeyPressMappingSet.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_KeyPressMappingSet.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_CachedComponentImage.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_Component.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_Component.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_ComponentListener.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_ComponentListener.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_ModalComponentManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_ModalComponentManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/desktop/juce_Desktop.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/desktop/juce_Desktop.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/desktop/juce_Displays.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/desktop/juce_Displays.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_Drawable.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_Drawable.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableComposite.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableComposite.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableImage.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableImage.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawablePath.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawablePath.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableRectangle.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableRectangle.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableShape.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableShape.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableText.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableText.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_SVGParser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_ContentSharer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_ContentSharer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_DirectoryContentsDisplayComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_DirectoryContentsDisplayComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_DirectoryContentsList.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_DirectoryContentsList.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileBrowserComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileBrowserComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileBrowserListener.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileChooser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileChooser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileChooserDialogBox.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileChooserDialogBox.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileListComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileListComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FilenameComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FilenameComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FilePreviewComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileSearchPathListComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileSearchPathListComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileTreeComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileTreeComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_ImagePreviewComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_ImagePreviewComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_CaretComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_CaretComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyboardFocusTraverser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyboardFocusTraverser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyListener.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyListener.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyPress.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyPress.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_ModifierKeys.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_ModifierKeys.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_SystemClipboard.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_TextEditorKeyMapper.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_TextInputTarget.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_AnimatedPosition.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_AnimatedPositionBehaviours.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentAnimator.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentAnimator.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentBoundsConstrainer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentBoundsConstrainer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentBuilder.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentBuilder.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentMovementWatcher.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentMovementWatcher.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ConcertinaPanel.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ConcertinaPanel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_FlexBox.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_FlexBox.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_FlexItem.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_Grid.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_Grid.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_GridItem.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_GridItem.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_GroupComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_GroupComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_MultiDocumentPanel.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_MultiDocumentPanel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableBorderComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableBorderComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableCornerComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableCornerComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableEdgeComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableEdgeComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ScrollBar.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ScrollBar.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_SidePanel.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_SidePanel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableLayoutManager.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableLayoutManager.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableLayoutResizerBar.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableLayoutResizerBar.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableObjectResizer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableObjectResizer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_TabbedButtonBar.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_TabbedButtonBar.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_TabbedComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_TabbedComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_Viewport.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_Viewport.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V1.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V1.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V2.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V2.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V3.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V3.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V4.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V4.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_BurgerMenuComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_BurgerMenuComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_MenuBarComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_MenuBarComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_MenuBarModel.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_MenuBarModel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_PopupMenu.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_PopupMenu.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_BubbleComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_BubbleComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_DropShadower.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_DropShadower.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_JUCESplashScreen.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_JUCESplashScreen.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_ComponentDragger.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_ComponentDragger.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_DragAndDropContainer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_DragAndDropContainer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_DragAndDropTarget.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_FileDragAndDropTarget.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_LassoComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseCursor.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseCursor.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseEvent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseEvent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseInactivityDetector.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseInactivityDetector.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseInputSource.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseInputSource.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseListener.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseListener.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_SelectedItemSet.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_TextDragAndDropTarget.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_TooltipClient.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_X11_DragAndDrop.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_X11_Symbols.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_X11_Symbols.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_XWindowSystem.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_XWindowSystem.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_android_ContentSharer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_android_FileChooser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_android_Windowing.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_common_MimeTypes.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_ios_ContentSharer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_ios_FileChooser.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_ios_UIViewComponentPeer.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_ios_Windowing.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_linux_FileChooser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_linux_Windowing.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_FileChooser.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_MainMenu.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_MouseCursor.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_NSViewComponentPeer.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_Windowing.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_MultiTouchMapper.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_win32_DragAndDrop.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_win32_FileChooser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_win32_ScopedThreadDPIAwarenessSetter.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_win32_Windowing.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_MarkerList.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_MarkerList.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeCoordinate.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeCoordinate.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeCoordinatePositioner.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeCoordinatePositioner.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeParallelogram.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeParallelogram.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativePoint.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativePoint.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativePointPath.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativePointPath.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeRectangle.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeRectangle.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_BooleanPropertyComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_BooleanPropertyComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_ButtonPropertyComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_ButtonPropertyComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_ChoicePropertyComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_ChoicePropertyComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_MultiChoicePropertyComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_MultiChoicePropertyComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_PropertyComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_PropertyComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_PropertyPanel.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_PropertyPanel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_SliderPropertyComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_SliderPropertyComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_TextPropertyComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_TextPropertyComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ComboBox.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ComboBox.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ImageComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ImageComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Label.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Label.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ListBox.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ListBox.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ProgressBar.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ProgressBar.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Slider.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Slider.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TableHeaderComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TableHeaderComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TableListBox.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TableListBox.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TextEditor.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TextEditor.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Toolbar.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Toolbar.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemFactory.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemPalette.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemPalette.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TreeView.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TreeView.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_AlertWindow.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_AlertWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_CallOutBox.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_CallOutBox.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ComponentPeer.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ComponentPeer.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_DialogWindow.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_DialogWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_DocumentWindow.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_DocumentWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_NativeMessageBox.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ResizableWindow.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ResizableWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ThreadWithProgressWindow.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ThreadWithProgressWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_TooltipWindow.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_TooltipWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_TopLevelWindow.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_TopLevelWindow.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/juce_gui_basics.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/juce_gui_basics.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/juce_gui_basics.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeDocument.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeDocument.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeEditorComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeEditorComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeTokeniser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CPlusPlusCodeTokeniser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CPlusPlusCodeTokeniser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CPlusPlusCodeTokeniserFunctions.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_LuaCodeTokeniser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_LuaCodeTokeniser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_XMLCodeTokeniser.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_XMLCodeTokeniser.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/documents/juce_FileBasedDocument.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/documents/juce_FileBasedDocument.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_ActiveXControlComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_AndroidViewComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_HWNDComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_NSViewComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_ScopedDPIAwarenessDisabler.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_UIViewComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_XEmbedComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_AnimatedAppComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_AnimatedAppComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_AppleRemote.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_BubbleMessageComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_BubbleMessageComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_ColourSelector.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_ColourSelector.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_KeyMappingEditorComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_KeyMappingEditorComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_LiveConstantEditor.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_LiveConstantEditor.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_PreferencesPanel.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_PreferencesPanel.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_PushNotifications.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_PushNotifications.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_RecentlyOpenedFilesList.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_RecentlyOpenedFilesList.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_SplashScreen.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_SplashScreen.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_SystemTrayIconComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_SystemTrayIconComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_WebBrowserComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_android_PushNotifications.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_android_WebBrowserComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_AndroidViewComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_ios_PushNotifications.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_ios_UIViewComponent.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_linux_X11_SystemTrayIcon.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_linux_X11_WebBrowserComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_linux_XEmbedComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_AppleRemote.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_CarbonViewWrapperComponent.h"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_NSViewComponent.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_PushNotifications.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_SystemTrayIcon.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_WebBrowserComponent.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_win32_ActiveXComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_win32_HWNDComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_win32_SystemTrayIcon.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_win32_WebBrowserComponent.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/juce_gui_extra.cpp"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/juce_gui_extra.mm"
    "../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/juce_gui_extra.h"
    "../../../JuceLibraryCode/include_juce_audio_basics.cpp"
    "../../../JuceLibraryCode/include_juce_audio_devices.cpp"
    "../../../JuceLibraryCode/include_juce_audio_formats.cpp"
    "../../../JuceLibraryCode/include_juce_audio_processors.cpp"
    "../../../JuceLibraryCode/include_juce_audio_utils.cpp"
    "../../../JuceLibraryCode/include_juce_core.cpp"
    "../../../JuceLibraryCode/include_juce_data_structures.cpp"
    "../../../JuceLibraryCode/include_juce_events.cpp"
    "../../../JuceLibraryCode/include_juce_graphics.cpp"
    "../../../JuceLibraryCode/include_juce_gui_basics.cpp"
    "../../../JuceLibraryCode/include_juce_gui_extra.cpp"
    "../../../JuceLibraryCode/JuceHeader.h"
)

set_source_files_properties("../../../Source/AudioSynthesiserDemo.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../Source/DemoUtilities.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../Source/AudioLiveScrollingDisplay.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/audio_play_head/juce_AudioPlayHead.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioChannelSet.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioChannelSet.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioDataConverters.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioDataConverters.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioProcessLoadMeasurer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioProcessLoadMeasurer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_AudioSampleBuffer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_FloatVectorOperations.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/buffers/juce_FloatVectorOperations.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiBuffer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiBuffer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiFile.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiFile.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiKeyboardState.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiKeyboardState.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiMessage.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiMessage.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiMessageSequence.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiMessageSequence.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiRPN.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/midi/juce_MidiRPN.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEInstrument.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEInstrument.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEMessages.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEMessages.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPENote.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPENote.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiserBase.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiserBase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiserVoice.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPESynthesiserVoice.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEUtils.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEUtils.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEValue.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEValue.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEZoneLayout.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/mpe/juce_MPEZoneLayout.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/native/juce_mac_CoreAudioLayouts.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_AudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_BufferingAudioSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_BufferingAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ChannelRemappingAudioSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ChannelRemappingAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_IIRFilterAudioSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_IIRFilterAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_MemoryAudioSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_MemoryAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_MixerAudioSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_MixerAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_PositionableAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ResamplingAudioSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ResamplingAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ReverbAudioSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ReverbAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ToneGeneratorAudioSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/sources/juce_ToneGeneratorAudioSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/synthesisers/juce_Synthesiser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/synthesisers/juce_Synthesiser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_ADSR.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_ADSR_test.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_Decibels.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_GenericInterpolator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_IIRFilter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_IIRFilter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_Interpolators.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_Interpolators.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_LagrangeInterpolator.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_Reverb.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_SmoothedValue.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_SmoothedValue.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/utilities/juce_WindowedSincInterpolator.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/juce_audio_basics.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/juce_audio_basics.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_basics/juce_audio_basics.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioDeviceManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioDeviceManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioIODevice.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioIODevice.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioIODeviceType.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_AudioIODeviceType.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/audio_io/juce_SystemAudioVolume.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPacket.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPackets.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPBytestreamInputHandler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPConversion.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPConverters.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPDispatcher.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPFactory.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPIterator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPMidi1ToBytestreamTranslator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPMidi1ToMidi2DefaultTranslator.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPMidi1ToMidi2DefaultTranslator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPProtocols.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPReceiver.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPSysEx7.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPSysEx7.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPTests.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPU32InputHandler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPUtils.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPUtils.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPView.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/ump/juce_UMPView.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/juce_MidiDevices.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/juce_MidiDevices.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/juce_MidiMessageCollector.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/midi_io/juce_MidiMessageCollector.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/AudioStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/AudioStreamBase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/AudioStreamBuilder.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/AudioStreamCallback.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/Definitions.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/LatencyTuner.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/Oboe.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/ResultWithValue.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/StabilizedCallback.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/Utilities.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/include/oboe/Version.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AAudioExtensions.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AAudioLoader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AAudioLoader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AudioStreamAAudio.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/aaudio/AudioStreamAAudio.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioClock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioSourceCaller.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioSourceCaller.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/AudioStreamBuilder.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/DataConversionFlowGraph.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/DataConversionFlowGraph.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FilterAudioStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FilterAudioStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockAdapter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockAdapter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockReader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockReader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockWriter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/FixedBlockWriter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/LatencyTuner.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/MonotonicCounter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/OboeDebug.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/QuirksManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/QuirksManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/SourceFloatCaller.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/SourceFloatCaller.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/SourceI16Caller.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/SourceI16Caller.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/StabilizedCallback.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/Trace.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/Trace.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/Utilities.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/common/Version.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoBuffer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoBuffer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoController.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoController.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoControllerBase.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoControllerBase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoControllerIndirect.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/fifo/FifoControllerIndirect.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/HyperbolicCosineWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/IntegerRatio.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/IntegerRatio.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/KaiserWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/LinearResampler.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/LinearResampler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/MultiChannelResampler.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/MultiChannelResampler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResampler.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResampler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResamplerMono.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResamplerMono.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResamplerStereo.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/PolyphaseResamplerStereo.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/SincResampler.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/SincResampler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/SincResamplerStereo.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/resampler/SincResamplerStereo.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ChannelCountConverter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ChannelCountConverter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ClipToRange.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ClipToRange.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/FlowGraphNode.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/FlowGraphNode.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ManyToMultiConverter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/ManyToMultiConverter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/MonoToMultiConverter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/MonoToMultiConverter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/MultiToMonoConverter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/MultiToMonoConverter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/RampLinear.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/RampLinear.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SampleRateConverter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SampleRateConverter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkFloat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkFloat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkI16.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkI16.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkI24.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SinkI24.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceFloat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceFloat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceI16.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceI16.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceI24.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/flowgraph/SourceI24.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioInputStreamOpenSLES.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioInputStreamOpenSLES.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioOutputStreamOpenSLES.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioOutputStreamOpenSLES.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioStreamBuffered.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioStreamBuffered.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioStreamOpenSLES.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/AudioStreamOpenSLES.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/EngineOpenSLES.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/EngineOpenSLES.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/OpenSLESUtilities.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/OpenSLESUtilities.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/OutputMixerOpenSLES.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/src/opensles/OutputMixerOpenSLES.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/CMakeLists.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/oboe/readme.md" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_Audio.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_HighPerformanceAudioHelpers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_Midi.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_Oboe.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_android_OpenSL.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_ios_Audio.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_ios_Audio.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_linux_ALSA.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_linux_Bela.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_linux_JackAudio.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_linux_Midi.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_mac_CoreAudio.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_mac_CoreMidi.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_MidiDataConcatenator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_win32_ASIO.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_win32_DirectSound.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_win32_Midi.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/native/juce_win32_WASAPI.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/sources/juce_AudioSourcePlayer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/sources/juce_AudioSourcePlayer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/sources/juce_AudioTransportSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/sources/juce_AudioTransportSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/juce_audio_devices.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/juce_audio_devices.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_devices/juce_audio_devices.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/all.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/bitmath.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/bitreader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/bitwriter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/cpu.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/crc.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/fixed.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/float.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/format.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/lpc.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/md5.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/memory.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/metadata.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/stream_encoder.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/stream_encoder_framing.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/private/window.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/protected/all.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/protected/stream_decoder.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/include/protected/stream_encoder.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/bitmath.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/bitreader.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/bitwriter.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/cpu.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/crc.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/fixed.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/float.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/format.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/lpc_flac.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/md5.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/memory.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/stream_decoder.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/stream_encoder.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/stream_encoder_framing.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/libFLAC/window_flac.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/all.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/alloc.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/assert.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/callback.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/compat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/endswap.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/export.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/Flac Licence.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/format.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/metadata.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/ordinals.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/stream_decoder.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/stream_encoder.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/flac/win_utf8_io.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/books/coupled/res_books_51.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/books/coupled/res_books_stereo.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/books/floor/floor_books.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/books/uncoupled/res_books_uncoupled.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/floor_all.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/psych_8.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/psych_11.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/psych_16.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/psych_44.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_8.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_16.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_44.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_44p51.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/residue_44u.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_8.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_11.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_16.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_22.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_32.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_44.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_44p51.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_44u.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/modes/setup_X.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/analysis.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/backends.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/bitrate.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/bitrate.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/block.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/codebook.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/codebook.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/codec_internal.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/envelope.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/envelope.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/floor0.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/floor1.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/highlevel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/info.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lookup.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lookup.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lookup_data.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lpc.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lpc.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lsp.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/lsp.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/mapping0.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/masking.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/mdct.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/mdct.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/misc.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/misc.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/os.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/psy.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/psy.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/registry.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/registry.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/res0.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/scales.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/sharedbook.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/smallft.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/smallft.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/synthesis.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/vorbisenc.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/vorbisfile.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/window.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/lib/window.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/libvorbis-1.3.7/README.md" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/bitwise.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/codec.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/config_types.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/crctable.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/framing.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/Ogg Vorbis Licence.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/ogg.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/os_types.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/vorbisenc.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/oggvorbis/vorbisfile.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_AiffAudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_AiffAudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_CoreAudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_CoreAudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_FlacAudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_FlacAudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_LAMEEncoderAudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_LAMEEncoderAudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_MP3AudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_MP3AudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_OggVorbisAudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_OggVorbisAudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_WavAudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_WavAudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_WindowsMediaAudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/codecs/juce_WindowsMediaAudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatReader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatReader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatReaderSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatReaderSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatWriter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioFormatWriter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioSubsectionReader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_AudioSubsectionReader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_BufferingAudioFormatReader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_BufferingAudioFormatReader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/format/juce_MemoryMappedAudioFormatReader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/sampler/juce_Sampler.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/sampler/juce_Sampler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/juce_audio_formats.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/juce_audio_formats.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_formats/juce_audio_formats.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format/juce_AudioPluginFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format/juce_AudioPluginFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format/juce_AudioPluginFormatManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format/juce_AudioPluginFormatManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/baseiids.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/classfactoryhelpers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fbuffer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fbuffer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fdebug.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fdebug.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fobject.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fobject.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fstreamer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fstreamer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fstring.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/fstring.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/updatehandler.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/source/updatehandler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/thread/include/flock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/thread/source/flock.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/LICENSE.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/base/README.md" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/conststringtable.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/conststringtable.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/coreiids.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/falignpop.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/falignpush.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/fplatform.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/fstrdefs.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ftypes.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/funknown.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/funknown.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/futils.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/fvariant.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ibstream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/icloneable.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ipersistent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ipluginbase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/istringresult.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/iupdatehandler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/smartpointer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/typesizecheck.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ustring.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/base/ustring.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/gui/iplugview.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/gui/iplugviewcontentscalesupport.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstattributes.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstaudioprocessor.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstautomationstate.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstchannelcontextinfo.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstcomponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstcontextmenu.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivsteditcontroller.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstevents.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivsthostapplication.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstinterappaudio.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstmessage.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstmidicontrollers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstmidilearn.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstnoteexpression.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstparameterchanges.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstphysicalui.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstpluginterfacesupport.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstplugview.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstprefetchablesupport.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstprocesscontext.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstrepresentation.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivsttestplugprovider.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/ivstunits.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/vstpshpack4.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/vstspeaker.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/vst/vsttypes.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/LICENSE.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/pluginterfaces/README.md" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/common/memorystream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/common/memorystream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/common/pluginview.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/common/pluginview.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/hosting/hostclasses.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/hosting/hostclasses.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/hosting/pluginterfacesupport.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/hosting/pluginterfacesupport.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstbus.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstbus.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstcomponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstcomponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstcomponentbase.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstcomponentbase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vsteditcontroller.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vsteditcontroller.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstinitiids.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstparameters.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstparameters.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstpresetfile.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/source/vst/vstpresetfile.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/LICENSE.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/public.sdk/README.md" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/JUCE_README.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/LICENSE.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/VST3_SDK/README.md" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_AU_Shared.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_AudioUnitPluginFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_AudioUnitPluginFormat.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_LADSPAPluginFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_LADSPAPluginFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_LegacyAudioParameter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VST3Common.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VST3Headers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VST3PluginFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VST3PluginFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VSTCommon.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VSTMidiEventList.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VSTPluginFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/format_types/juce_VSTPluginFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioPluginInstance.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioPluginInstance.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessor.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessor.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorEditor.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorEditor.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorGraph.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorGraph.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorListener.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorParameter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorParameterGroup.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_AudioProcessorParameterGroup.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_GenericAudioProcessorEditor.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_GenericAudioProcessorEditor.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_PluginDescription.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/processors/juce_PluginDescription.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_KnownPluginList.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_KnownPluginList.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_PluginDirectoryScanner.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_PluginDirectoryScanner.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_PluginListComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/scanning/juce_PluginListComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterBool.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterBool.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterChoice.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterChoice.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterFloat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterFloat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterInt.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioParameterInt.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioProcessorParameterWithID.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioProcessorParameterWithID.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioProcessorValueTreeState.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_AudioProcessorValueTreeState.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_ParameterAttachments.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_ParameterAttachments.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_PluginHostType.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_PluginHostType.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_RangedAudioParameter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/utilities/juce_RangedAudioParameter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/juce_audio_processors.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/juce_audio_processors.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_processors/juce_audio_processors.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/audio_cd/juce_AudioCDBurner.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/audio_cd/juce_AudioCDReader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/audio_cd/juce_AudioCDReader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioAppComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioAppComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioDeviceSelectorComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioDeviceSelectorComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnail.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnail.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnailBase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnailCache.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioThumbnailCache.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioVisualiserComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_AudioVisualiserComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_BluetoothMidiDevicePairingDialogue.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_MidiKeyboardComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/gui/juce_MidiKeyboardComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_android_BluetoothMidiDevicePairingDialogue.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_ios_BluetoothMidiDevicePairingDialogue.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_linux_AudioCDReader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_linux_BluetoothMidiDevicePairingDialogue.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_mac_AudioCDBurner.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_mac_AudioCDReader.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_mac_BluetoothMidiDevicePairingDialogue.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_win_BluetoothMidiDevicePairingDialogue.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_win32_AudioCDBurner.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/native/juce_win32_AudioCDReader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/players/juce_AudioProcessorPlayer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/players/juce_AudioProcessorPlayer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/players/juce_SoundPlayer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/players/juce_SoundPlayer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/juce_audio_utils.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/juce_audio_utils.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_audio_utils/juce_audio_utils.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_AbstractFifo.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_AbstractFifo.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_Array.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ArrayAllocationBase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ArrayBase.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ArrayBase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_DynamicObject.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_DynamicObject.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ElementComparator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_HashMap.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_HashMap_test.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_LinkedListPointer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ListenerList.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_NamedValueSet.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_NamedValueSet.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_OwnedArray.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_OwnedArray.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_PropertySet.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_PropertySet.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ReferenceCountedArray.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ReferenceCountedArray.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_ScopedValueSetter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_SortedSet.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_SparseSet.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_SparseSet.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_Variant.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/containers/juce_Variant.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_DirectoryIterator.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_DirectoryIterator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_File.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_File.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileFilter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileFilter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileInputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileInputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileOutputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileOutputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileSearchPath.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_FileSearchPath.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_MemoryMappedFile.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_RangedDirectoryIterator.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_RangedDirectoryIterator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_TemporaryFile.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_TemporaryFile.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_WildcardFileFilter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/files/juce_WildcardFileFilter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/javascript/juce_Javascript.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/javascript/juce_Javascript.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/javascript/juce_JSON.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/javascript/juce_JSON.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/logging/juce_FileLogger.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/logging/juce_FileLogger.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/logging/juce_Logger.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/logging/juce_Logger.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_BigInteger.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_BigInteger.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Expression.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Expression.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_MathsFunctions.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_NormalisableRange.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Random.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Random.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_Range.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/maths/juce_StatisticsAccumulator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_AllocationHooks.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_AllocationHooks.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_Atomic.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_ByteOrder.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_ContainerDeletePolicy.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_HeapBlock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_HeavyweightLeakedObjectDetector.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_LeakedObjectDetector.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_Memory.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_MemoryBlock.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_MemoryBlock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_OptionalScopedPointer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_ReferenceCountedObject.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_ScopedPointer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_SharedResourcePointer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_Singleton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/memory/juce_WeakReference.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_ConsoleApplication.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_ConsoleApplication.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_Result.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_Result.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_RuntimePermissions.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_RuntimePermissions.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_Uuid.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_Uuid.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/misc/juce_WindowsRegistry.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/java/README.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_Files.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_JNIHelpers.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_JNIHelpers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_Misc.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_Network.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_RuntimePermissions.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_SystemStats.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_android_Threads.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_BasicNativeHeaders.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_curl_Network.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_intel_SharedCode.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_CommonFile.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_Files.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_Network.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_SystemStats.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_linux_Threads.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_CFHelpers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_ClangBugWorkaround.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_Files.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_Network.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_ObjCHelpers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_Strings.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_SystemStats.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_mac_Threads.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_posix_IPAddress.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_posix_NamedPipe.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_posix_SharedCode.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_wasm_SystemStats.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_ComSmartPtr.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_Files.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_Network.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_Registry.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_SystemStats.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/native/juce_win32_Threads.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_IPAddress.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_IPAddress.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_MACAddress.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_MACAddress.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_NamedPipe.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_NamedPipe.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_Socket.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_Socket.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_URL.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_URL.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_WebInputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/network/juce_WebInputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_BufferedInputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_BufferedInputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_FileInputSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_FileInputSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_InputSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_InputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_InputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_MemoryInputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_MemoryInputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_MemoryOutputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_MemoryOutputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_OutputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_OutputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_SubregionStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_SubregionStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_URLInputSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/streams/juce_URLInputSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_CompilerSupport.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_CompilerWarnings.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_PlatformDefs.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_StandardHeader.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_SystemStats.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_SystemStats.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/system/juce_TargetPlatform.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_Base64.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_Base64.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharacterFunctions.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharacterFunctions.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharPointer_ASCII.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharPointer_UTF8.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharPointer_UTF16.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_CharPointer_UTF32.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_Identifier.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_Identifier.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_LocalisedStrings.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_LocalisedStrings.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_NewLine.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_String.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_String.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringArray.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringArray.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringPairArray.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringPairArray.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringPool.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringPool.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_StringRef.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_TextDiff.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/text/juce_TextDiff.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ChildProcess.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ChildProcess.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_CriticalSection.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_DynamicLibrary.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_HighResolutionTimer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_HighResolutionTimer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_InterProcessLock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_Process.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ReadWriteLock.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ReadWriteLock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ScopedLock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ScopedReadLock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ScopedWriteLock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_SpinLock.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_Thread.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_Thread.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ThreadLocalValue.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ThreadPool.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_ThreadPool.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_TimeSliceThread.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_TimeSliceThread.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_WaitableEvent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/threads/juce_WaitableEvent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_PerformanceCounter.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_PerformanceCounter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_RelativeTime.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_RelativeTime.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_Time.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/time/juce_Time.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/unit_tests/juce_UnitTest.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/unit_tests/juce_UnitTest.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/unit_tests/juce_UnitTestCategories.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/xml/juce_XmlDocument.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/xml/juce_XmlDocument.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/xml/juce_XmlElement.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/xml/juce_XmlElement.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/adler32.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/compress.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/crc32.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/crc32.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/deflate.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/deflate.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/infback.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inffast.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inffast.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inffixed.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inflate.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inflate.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inftrees.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/inftrees.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/trees.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/trees.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/uncompr.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zconf.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zconf.in.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zlib.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zutil.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/zlib/zutil.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_GZIPCompressorOutputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_GZIPCompressorOutputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_GZIPDecompressorInputStream.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_GZIPDecompressorInputStream.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_ZipFile.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/zip/juce_ZipFile.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/juce_core.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/juce_core.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_core/juce_core.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/app_properties/juce_ApplicationProperties.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/app_properties/juce_ApplicationProperties.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/app_properties/juce_PropertiesFile.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/app_properties/juce_PropertiesFile.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/undomanager/juce_UndoableAction.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/undomanager/juce_UndoManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/undomanager/juce_UndoManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_CachedValue.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_CachedValue.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_Value.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_Value.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueTree.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueTree.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueTreeSynchroniser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueTreeSynchroniser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueWithDefault.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/values/juce_ValueWithDefault.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/juce_data_structures.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/juce_data_structures.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_data_structures/juce_data_structures.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ActionBroadcaster.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ActionBroadcaster.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ActionListener.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_AsyncUpdater.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_AsyncUpdater.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ChangeBroadcaster.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ChangeBroadcaster.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/broadcasters/juce_ChangeListener.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_ConnectedChildProcess.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_ConnectedChildProcess.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_InterprocessConnection.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_InterprocessConnection.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_InterprocessConnectionServer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_InterprocessConnectionServer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_NetworkServiceDiscovery.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/interprocess/juce_NetworkServiceDiscovery.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_ApplicationBase.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_ApplicationBase.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_CallbackMessage.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_DeletedAtShutdown.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_DeletedAtShutdown.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_Initialisation.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_Message.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MessageListener.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MessageListener.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MessageManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MessageManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_MountedVolumeListChangeDetector.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/messages/juce_NotificationType.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_android_Messaging.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_ios_MessageManager.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_linux_EventLoop.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_linux_Messaging.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_mac_MessageManager.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_osx_MessageQueue.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_win32_HiddenMessageWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_win32_Messaging.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_win32_WinRTWrapper.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/native/juce_win32_WinRTWrapper.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/timers/juce_MultiTimer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/timers/juce_MultiTimer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/timers/juce_Timer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/timers/juce_Timer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/juce_events.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/juce_events.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_events/juce_events.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_Colour.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_Colour.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_ColourGradient.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_ColourGradient.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_Colours.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_Colours.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_FillType.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_FillType.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/colour/juce_PixelFormats.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_GraphicsContext.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_GraphicsContext.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsContext.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsPostScriptRenderer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsPostScriptRenderer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsSoftwareRenderer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/contexts/juce_LowLevelGraphicsSoftwareRenderer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_DropShadowEffect.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_DropShadowEffect.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_GlowEffect.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_GlowEffect.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/effects/juce_ImageEffectFilter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_AttributedString.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_AttributedString.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_CustomTypeface.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_CustomTypeface.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_Font.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_Font.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_GlyphArrangement.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_GlyphArrangement.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_TextLayout.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_TextLayout.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_Typeface.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/fonts/juce_Typeface.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_AffineTransform.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_AffineTransform.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_BorderSize.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_EdgeTable.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_EdgeTable.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Line.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Parallelogram.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Path.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Path.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_PathIterator.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_PathIterator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_PathStrokeType.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_PathStrokeType.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Point.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_Rectangle.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/geometry/juce_RectangleList.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/cderror.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/changes to libjpeg for JUCE.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcapimin.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcapistd.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jccoefct.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jccolor.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcdctmgr.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jchuff.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jchuff.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcinit.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcmainct.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcmarker.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcmaster.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcomapi.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jconfig.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcparam.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcphuff.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcprepct.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jcsample.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jctrans.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdapimin.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdapistd.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdatasrc.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdcoefct.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdcolor.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdct.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jddctmgr.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdhuff.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdhuff.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdinput.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdmainct.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdmarker.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdmaster.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdmerge.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdphuff.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdpostct.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdsample.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jdtrans.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jerror.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jerror.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jfdctflt.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jfdctfst.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jfdctint.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jidctflt.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jidctfst.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jidctint.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jidctred.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jinclude.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jmemmgr.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jmemnobs.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jmemsys.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jmorecfg.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jpegint.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jpeglib.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jquant1.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jquant2.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jutils.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/jversion.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/transupp.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/jpglib/transupp.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/libpng_readme.txt" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/png.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/png.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngconf.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngdebug.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngerror.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngget.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pnginfo.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngmem.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngpread.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngpriv.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngread.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngrio.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngrtran.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngrutil.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngset.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngstruct.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngtrans.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngwio.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngwrite.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngwtran.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/pnglib/pngwutil.c" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/juce_GIFLoader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/juce_JPEGLoader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/image_formats/juce_PNGLoader.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_Image.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_Image.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageCache.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageCache.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageConvolutionKernel.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageConvolutionKernel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageFileFormat.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/images/juce_ImageFileFormat.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_android_Fonts.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_android_GraphicsContext.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_android_IconHelpers.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_freetype_Fonts.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_linux_Fonts.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_linux_IconHelpers.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_CoreGraphicsContext.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_CoreGraphicsContext.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_CoreGraphicsHelpers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_Fonts.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_mac_IconHelpers.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_RenderingHelpers.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_Direct2DGraphicsContext.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_Direct2DGraphicsContext.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_DirectWriteTypeface.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_DirectWriteTypeLayout.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_Fonts.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/native/juce_win32_IconHelpers.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/placement/juce_Justification.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/placement/juce_RectanglePlacement.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/placement/juce_RectanglePlacement.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/juce_graphics.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/juce_graphics.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_graphics/juce_graphics.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/application/juce_Application.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/application/juce_Application.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ArrowButton.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ArrowButton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_Button.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_Button.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_DrawableButton.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_DrawableButton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_HyperlinkButton.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_HyperlinkButton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ImageButton.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ImageButton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ShapeButton.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ShapeButton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_TextButton.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_TextButton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ToggleButton.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ToggleButton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ToolbarButton.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/buttons/juce_ToolbarButton.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandID.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandInfo.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandInfo.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandTarget.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_ApplicationCommandTarget.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_KeyPressMappingSet.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/commands/juce_KeyPressMappingSet.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_CachedComponentImage.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_Component.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_Component.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_ComponentListener.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_ComponentListener.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_ModalComponentManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/components/juce_ModalComponentManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/desktop/juce_Desktop.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/desktop/juce_Desktop.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/desktop/juce_Displays.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/desktop/juce_Displays.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_Drawable.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_Drawable.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableComposite.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableComposite.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableImage.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableImage.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawablePath.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawablePath.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableRectangle.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableRectangle.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableShape.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableShape.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableText.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_DrawableText.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/drawables/juce_SVGParser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_ContentSharer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_ContentSharer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_DirectoryContentsDisplayComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_DirectoryContentsDisplayComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_DirectoryContentsList.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_DirectoryContentsList.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileBrowserComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileBrowserComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileBrowserListener.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileChooser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileChooser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileChooserDialogBox.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileChooserDialogBox.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileListComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileListComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FilenameComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FilenameComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FilePreviewComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileSearchPathListComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileSearchPathListComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileTreeComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_FileTreeComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_ImagePreviewComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/filebrowser/juce_ImagePreviewComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_CaretComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_CaretComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyboardFocusTraverser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyboardFocusTraverser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyListener.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyListener.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyPress.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_KeyPress.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_ModifierKeys.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_ModifierKeys.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_SystemClipboard.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_TextEditorKeyMapper.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/keyboard/juce_TextInputTarget.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_AnimatedPosition.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_AnimatedPositionBehaviours.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentAnimator.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentAnimator.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentBoundsConstrainer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentBoundsConstrainer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentBuilder.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentBuilder.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentMovementWatcher.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ComponentMovementWatcher.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ConcertinaPanel.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ConcertinaPanel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_FlexBox.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_FlexBox.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_FlexItem.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_Grid.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_Grid.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_GridItem.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_GridItem.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_GroupComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_GroupComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_MultiDocumentPanel.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_MultiDocumentPanel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableBorderComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableBorderComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableCornerComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableCornerComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableEdgeComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ResizableEdgeComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ScrollBar.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_ScrollBar.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_SidePanel.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_SidePanel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableLayoutManager.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableLayoutManager.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableLayoutResizerBar.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableLayoutResizerBar.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableObjectResizer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_StretchableObjectResizer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_TabbedButtonBar.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_TabbedButtonBar.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_TabbedComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_TabbedComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_Viewport.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/layout/juce_Viewport.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V1.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V1.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V2.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V2.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V3.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V3.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V4.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/lookandfeel/juce_LookAndFeel_V4.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_BurgerMenuComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_BurgerMenuComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_MenuBarComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_MenuBarComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_MenuBarModel.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_MenuBarModel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_PopupMenu.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/menus/juce_PopupMenu.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_BubbleComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_BubbleComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_DropShadower.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_DropShadower.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_JUCESplashScreen.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/misc/juce_JUCESplashScreen.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_ComponentDragger.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_ComponentDragger.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_DragAndDropContainer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_DragAndDropContainer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_DragAndDropTarget.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_FileDragAndDropTarget.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_LassoComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseCursor.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseCursor.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseEvent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseEvent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseInactivityDetector.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseInactivityDetector.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseInputSource.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseInputSource.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseListener.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_MouseListener.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_SelectedItemSet.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_TextDragAndDropTarget.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/mouse/juce_TooltipClient.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_X11_DragAndDrop.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_X11_Symbols.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_X11_Symbols.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_XWindowSystem.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/x11/juce_linux_XWindowSystem.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_android_ContentSharer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_android_FileChooser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_android_Windowing.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_common_MimeTypes.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_ios_ContentSharer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_ios_FileChooser.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_ios_UIViewComponentPeer.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_ios_Windowing.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_linux_FileChooser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_linux_Windowing.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_FileChooser.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_MainMenu.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_MouseCursor.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_NSViewComponentPeer.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_mac_Windowing.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_MultiTouchMapper.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_win32_DragAndDrop.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_win32_FileChooser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_win32_ScopedThreadDPIAwarenessSetter.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/native/juce_win32_Windowing.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_MarkerList.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_MarkerList.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeCoordinate.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeCoordinate.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeCoordinatePositioner.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeCoordinatePositioner.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeParallelogram.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeParallelogram.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativePoint.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativePoint.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativePointPath.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativePointPath.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeRectangle.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/positioning/juce_RelativeRectangle.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_BooleanPropertyComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_BooleanPropertyComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_ButtonPropertyComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_ButtonPropertyComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_ChoicePropertyComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_ChoicePropertyComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_MultiChoicePropertyComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_MultiChoicePropertyComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_PropertyComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_PropertyComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_PropertyPanel.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_PropertyPanel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_SliderPropertyComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_SliderPropertyComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_TextPropertyComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/properties/juce_TextPropertyComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ComboBox.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ComboBox.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ImageComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ImageComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Label.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Label.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ListBox.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ListBox.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ProgressBar.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ProgressBar.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Slider.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Slider.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TableHeaderComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TableHeaderComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TableListBox.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TableListBox.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TextEditor.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TextEditor.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Toolbar.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_Toolbar.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemFactory.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemPalette.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_ToolbarItemPalette.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TreeView.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/widgets/juce_TreeView.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_AlertWindow.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_AlertWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_CallOutBox.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_CallOutBox.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ComponentPeer.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ComponentPeer.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_DialogWindow.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_DialogWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_DocumentWindow.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_DocumentWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_NativeMessageBox.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ResizableWindow.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ResizableWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ThreadWithProgressWindow.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_ThreadWithProgressWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_TooltipWindow.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_TooltipWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_TopLevelWindow.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/windows/juce_TopLevelWindow.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/juce_gui_basics.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/juce_gui_basics.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_basics/juce_gui_basics.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeDocument.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeDocument.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeEditorComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeEditorComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CodeTokeniser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CPlusPlusCodeTokeniser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CPlusPlusCodeTokeniser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_CPlusPlusCodeTokeniserFunctions.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_LuaCodeTokeniser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_LuaCodeTokeniser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_XMLCodeTokeniser.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/code_editor/juce_XMLCodeTokeniser.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/documents/juce_FileBasedDocument.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/documents/juce_FileBasedDocument.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_ActiveXControlComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_AndroidViewComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_HWNDComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_NSViewComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_ScopedDPIAwarenessDisabler.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_UIViewComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/embedding/juce_XEmbedComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_AnimatedAppComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_AnimatedAppComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_AppleRemote.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_BubbleMessageComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_BubbleMessageComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_ColourSelector.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_ColourSelector.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_KeyMappingEditorComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_KeyMappingEditorComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_LiveConstantEditor.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_LiveConstantEditor.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_PreferencesPanel.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_PreferencesPanel.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_PushNotifications.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_PushNotifications.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_RecentlyOpenedFilesList.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_RecentlyOpenedFilesList.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_SplashScreen.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_SplashScreen.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_SystemTrayIconComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_SystemTrayIconComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/misc/juce_WebBrowserComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_android_PushNotifications.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_android_WebBrowserComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_AndroidViewComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_ios_PushNotifications.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_ios_UIViewComponent.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_linux_X11_SystemTrayIcon.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_linux_X11_WebBrowserComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_linux_XEmbedComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_AppleRemote.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_CarbonViewWrapperComponent.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_NSViewComponent.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_PushNotifications.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_SystemTrayIcon.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_mac_WebBrowserComponent.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_win32_ActiveXComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_win32_HWNDComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_win32_SystemTrayIcon.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/native/juce_win32_WebBrowserComponent.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/juce_gui_extra.cpp" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/juce_gui_extra.mm" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../../../../../../../../Program Files/JUCE/modules/juce_gui_extra/juce_gui_extra.h" PROPERTIES HEADER_FILE_ONLY TRUE)
set_source_files_properties("../../../JuceLibraryCode/JuceHeader.h" PROPERTIES HEADER_FILE_ONLY TRUE)

target_compile_options( ${BINARY_NAME} PRIVATE "-fsigned-char" )

if( JUCE_BUILD_CONFIGURATION MATCHES "DEBUG" )
    target_compile_options( ${BINARY_NAME} PRIVATE)
endif()

if( JUCE_BUILD_CONFIGURATION MATCHES "RELEASE" )
    target_compile_options( ${BINARY_NAME} PRIVATE)
endif()

find_library(log "log")
find_library(android "android")
find_library(glesv2 "GLESv2")
find_library(egl "EGL")

target_link_libraries( ${BINARY_NAME}

    ${log}
    ${android}
    ${glesv2}
    ${egl}
    "cpufeatures"
    "oboe"
)
