# Nano Calculator (Android)

Simple, dark-themed nano calculator app — Kotlin + View system.

## GitHub par upload karne k steps

1. GitHub par login karein aur naya **repository** banayein (e.g. `nano-calculator`).
2. Is poore `NanoCalculator` folder ka content us repository mein push/upload kar dein
   (GitHub website se "Add file → Upload files" ya `git push` k zariye).
3. Repository mein jaa kar `app/build.gradle.kts` open karein. `debug { ... }` block mein
   agar `applicationIdSuffix` ya `versionNameSuffix` jaisi lines maujood hain jo aap nahi
   chahte, unhe remove/comment kar k **Commit changes** kar dein.
4. GitHub **Actions** tab par jayein — `Build Nano Calculator APK` workflow khud chalegi
   (push par automatically trigger hoti hai), ya `Run workflow` button se manually chala dein.
5. Workflow complete hone k baad, us run k **Artifacts** section mein
   `NanoCalculator-debug-apk` milega — download kar k apna APK install kar saktay hain.

## Notes
- Ye project Gradle wrapper files (`gradlew`) include nahi karta; workflow seedha
  `gradle/actions/setup-gradle` se Gradle install kar k build karta hai, is liye
  `gradlew` na hone se bhi build chal jayegi.
- Release/signed APK chahiye ho to `build.yml` mein `assembleRelease` add kar k
  signing config alag se set karni hogi.
