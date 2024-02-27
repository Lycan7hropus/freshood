This is a Kotlin Multiplatform project targeting Android, iOS, Web, Server.

* `/composeApp` is for code that will be shared across your Compose Multiplatform applications.
  It contains several subfolders:
  - `commonMain` is for code that’s common for all targets.
  - Other folders are for Kotlin code that will be compiled for only the platform indicated in the folder name.
    For example, if you want to use Apple’s CoreCrypto for the iOS part of your Kotlin app,
    `iosMain` would be the right folder for such calls.

* `/iosApp` contains iOS applications. Even if you’re sharing your UI with Compose Multiplatform, 
  you need this entry point for your iOS app. This is also where you should add SwiftUI code for your project.

* `/server` is for the Ktor server application.

* `/shared` is for the code that will be shared between all targets in the project.
  The most important subfolder is `commonMain`. If preferred, you can add code to the platform-specific folders here too.


Learn more about [Kotlin Multiplatform](https://www.jetbrains.com/help/kotlin-multiplatform-dev/get-started.html),
[Compose Multiplatform](https://github.com/JetBrains/compose-multiplatform/#compose-multiplatform),
[Kotlin/Wasm](https://kotl.in/wasm/)…

**Note:** Compose/Web is Experimental and may be changed at any time. Use it only for evaluation purposes.
We would appreciate your feedback on Compose/Web and Kotlin/Wasm in the public Slack channel [#compose-web](https://slack-chats.kotlinlang.org/c/compose-web).
If you face any issues, please report them on [GitHub](https://github.com/JetBrains/compose-multiplatform/issues).

You can open the web application by running the `:composeApp:wasmJsBrowserDevelopmentRun` Gradle task.



[<img alt="forthebadge" height="24" src="https://forthebadge.com/images/featured/featured-contains-cat-gifs.svg"/>](https://forthebadge.com)[<img alt="forthebadge" height="24" src="https://forthebadge.com/images/badges/works-on-my-machine.svg"/>](https://forthebadge.com) <img alt="version-badge.svg" height="24" src="assets/version-badge.svg"/>
![fresh-back.png](assets%2Ffresh-back.png)


### This project is still under development. Features and documentation are subject to change.

### Overview

Goal of **Fresh Near Me** is to connect consumers directly with local producers, making it easy for everyone to access and enjoy fresh, locally-grown food. This platform is about supporting local communities and promoting healthier, sustainable food choices.

### Why fresh near me?
Michigan State University [article](https://www.canr.msu.edu/news/seven-benefits-of-local-food) underscores the advantages of consuming locally sourced food:

- **Full Flavor**: Local produce, harvested at peak ripeness, offers superior flavor compared to goods harvested early for shipping.


- **Nutrient Rich**: The short journey from farm to table means local foods are likely to have higher nutrient retention.


- **Boosts Local Economy**: Spending on local foods contributes significantly to the local economy. Research of local
  economic flows has demonstrated that the food system in
  Michigan [contributed $680 million to state earnings in 2011.](https://www.canr.msu.edu/cea/uploads/files/valuingmilocalfoodsystem.pdf)


- **Environmental Advantages**: Local sourcing minimizes the environmental footprint associated with long-distance transportation, supporting sustainability in agriculture.


- **Food Safety**: Reduced supply chain length enhances food safety by limiting contamination risks.


- **Direct Transparency**: The platform facilitates direct interactions between consumers and producers, offering deeper insight into food production methods.

Furthermore, [research](https://www.cals.iastate.edu/news/2022/research-shows-significant-environmental-benefits-local-food-production) from Iowa State University highlights that large-scale production model had significantly greater global warming potential in all stages of food production and
distribution than that of the medium- and small-scale production models.
Typical **local vegetable production** produces **less than half the emissions** and use 10% of the water than that of
conventional food systems.
