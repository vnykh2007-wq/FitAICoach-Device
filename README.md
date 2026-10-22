# FitAI Coach

Native SwiftUI iPhone and Apple Watch workout coach. Local rule engine,
HealthKit, workout mirroring, WatchConnectivity, JSON storage and XCTest.

This cloud build copy has an EMPTY profile, history, calendar and test results.
No personal health seed or local diagnostic reports are included. Unit test
samples are synthetic fixtures only, never live sensor readings.

Generate with `xcodegen generate`; run `swift test` on macOS. Schemes:
`FitAICoach` and `FitAICoachWatch`. Simulator workflows build apps that cannot
be installed on physical devices. The manual device-build.yml workflow instead
targets physical iOS/watchOS ARM64, verifies Mach-O platforms and packages an
UNSIGNED IPA for subsequent Apple signing. It has not yet been run successfully.
No signing certificates, profiles or Apple Account credentials are included.
An unsigned IPA cannot be installed directly. Actual device signing,
HealthKit permissions, background recovery and pairing require device testing.
There is no paid API, server or required registration in the app.

CI builds the ordinary repository files directly and checks simulator launches.
