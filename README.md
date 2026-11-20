# Tapping Test for MS Assessment

A smartphone finger-tapping test for assessing motor fatigue in Multiple Sclerosis patients. Built as a prototype during the TUM Project Week (2024).

## How it works

The patient taps on the phone for 30 seconds while the app records the accelerometer (~50 Hz). Afterwards it detects taps as prominent peaks in the acceleration magnitude and reports:

- **Mean frequency [Hz]**: taps per second over the whole test
- **Frequency loss [%]**: drop in tapping rate between the first and last 5 seconds (a measure of fatigue)
- **Signal-to-noise [%]**: share of detected peaks that count as real taps

## Tech

C# / Xamarin.Forms with Xamarin.Essentials for sensor access, with Android, iOS and UWP targets. The test logic is in [`BoldiMert/BoldiMert/MainPage.xaml.cs`](BoldiMert/BoldiMert/MainPage.xaml.cs).

Open `BoldiMert.sln` in Visual Studio with the Xamarin workload to build. Note that Xamarin.Forms has reached end of life, so this is kept as an early-stage prototype.
