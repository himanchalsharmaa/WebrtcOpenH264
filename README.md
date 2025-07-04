# WebrtcOpenH264

This repository contains libwebrtc.so built using a modified version of Unity's build script(https://github.com/Unity-Technologies/com.unity.webrtc/blob/main/BuildScripts~/build_libwebrtc_win.cmd) which contains Cisco's OpenH264 that is used by the Unity's WebRTC plugin(again built using Unity's build script(https://github.com/Unity-Technologies/com.unity.webrtc/blob/main/BuildScripts~/build_plugin_win.cmd) to support OpenH264 software encoder/decoder. It is quite tricky to build libwebrtc, feel free to use this in accordance with Cisco's License.
<br/>
The reason for these builds: <br/>
Unity's WebRTC only supports Nvidia Hardware H264 Encoder/Decoder and Meta Quest 3 does support H264 hardware encoding. If your decoder device doesn't have an Nvidia GPU, it would force Meta Quest 3 to use Vp8 software encoder which is very CPU intensive. This DLL allows Webrtc to negotiate H264 on Intel/AMD and other GPUs via OpenH264, hence reducing the CPU workload on Main thread.
<br/>
License: https://github.com/himanchalsharmaa/WebrtcOpenH264/blob/main/LICENSE.txt
