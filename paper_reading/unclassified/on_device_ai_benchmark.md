https://arxiv.org/pdf/1910.06663.pdf

This paper is a survey about various frameworks/libraries/hardware accelators to improve the on-device ML inference performance.

A significant part of this paper is about comparing different NPU(neueral nets processing unit) chips, which I do not care about.

This paper introduces a lit bit about the history about TF Lite and NNAPI:

*   TF Lite has two parts: model converter and interpreter
*   Converter converts a normal TF model to a TF Lite one, including some optimization and reformat
*   Interpreter is a runtime on device, can be easily intergrated into different languages/platforms
*   NNAPI is a middle layer between TF Lite and hardwares, introduced in api 27
*   NNAPI can distribute computation works to proper hardwares available on the devices(GPU, DSP, NPU, etc.), if no available devices, it will use CPU
*   Before NNAPI, TF Lite can use Delegate will take advantage of hardware accelators

So basically for app develoeprs, just use TF Lite and it will take care of the rest.

A nice blog about TF Lite and NNAPI: https://jackwish.net/2018/on-android-nnapi.html
